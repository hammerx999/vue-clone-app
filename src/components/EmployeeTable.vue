<template>
    <div id="employee-table">
        <p v-if="employees.length < 1" class="empty-table">
            No Employee
        </p>
        <table>
            <thead>
                <tr>
                    <th>Employee name</th>
                    <th>Employee email</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="employee in employees" :key="employee.id">
                    <td v-if="editing === employee.id">
                            <input type="text" v-model="employee.name">
                    </td>
                    <td v-else>{{ employee.name }}</td>

                    <td v-if="editing === employee.id">
                            <input type="text" v-model="employee.email">
                    </td>
                    <td v-else>{{ employee.email }}</td>
                  
                    <td v-if="editing === employee.id"> 
                        <button @click="editEmployee(employee)" >Save</button> <spacer></spacer>
                        <button class="muted-button" @click="cancelEdit(employee)">Cancel</button>
                        
                    </td>
                    <td v-else>
                       
                        <button @click="editMode(employee)" >Edit</button> <spacer></spacer>
                        <button @click="$emit('delete:employee', employee.id)">Delete</button>
                    </td>
                </tr>
              
                    
            </tbody>
        </table>

    </div>
</template>

<script>
export default {
    name: 'employee-table',
    data() {
       return {
        editing:null,
       }
    },
    methods: {
        editMode(employee) {
            this.cachedEmployee = Object.assign({}, employee)
            this.editing = employee.id
        },
        
        cancelEdit(employee){
            Object.assign(employee, this.cachedEmployee)
            this.editing = null
        },

        editEmployee(employee) {
            if (employee.name === '' || employee.email === '') return
            this.$emit('edit:employee', employee.id, employee)
            this.editing = null
        }
    },
    props: {
        employees: Array
    }
}
</script>

<style scoped>
    
    button {
        background:  #2d7b7c;
        border: 1 PX solid #2d7b7c;
    }
    .empty-table {
        font-weight: bold;
        font-size: 1.3rem;
        background: orange;
        color: #000;
        padding: .5rem 1rem;
        width: 57.5%;
    }

    table {
    font-family: Arial, Helvetica, sans-serif;
    border-collapse: collapse;
    width: 70%;
    }

    table td, table th {
    border: 1px solid #ddd;
    padding: 8px;
    }

    table tr:nth-child(even){background-color: #f2f2f2;}

    table tr:hover {background-color: #ddd;}

    table th {
    padding-top: 12px;
    padding-bottom: 12px;
    text-align: left;
    background-color: #397f83;
    color: white;
    }
</style>