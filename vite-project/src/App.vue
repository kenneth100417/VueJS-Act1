<script setup>
    import { ref } from 'vue';

    const firstname = ref('');
    const middlename = ref('');
    const lastname = ref('');
    const yearlevel = ref('');
    const course = ref('');
    const block = ref('');
</script>

<template>
    <div style="margin:  10% 35%; border: 1px solid gray; padding: 10px 40px;border-radius: 15px">
        <div style="display:flex; justify-content: center;">
            <h2>Student Form</h2>
        </div>
        <div style="display: flex; flex-direction: column;">
            <input style="margin-top: 5px" type="text" v-model="firstname" placeholder="Firstname">
            <input style="margin-top: 5px" type="text" v-model="middlename" placeholder="Middlename">
            <input style="margin-top: 5px" type="text" v-model="lastname" placeholder="Lastname">

            <select style="margin-top: 5px" v-model="course" title="">
                <option value='' selected>Select Course</option>
                <option value='BSIT'>BSIT</option>
                <option value='BSA'>BSA</option>
                <option value='BSA'>BSE</option>
                <option value='BSIT'>BSIS</option>
                <option value='BSIT'>BSCS</option>
                <option value='BSIT'>BSIT</option>
                <option value='BSIT'>BSIT</option>
            </select>
            <select style="margin-top: 5px" v-model="yearlevel" title="">
                <option value='' selected>Select Year Level</option>
                <option value='I'>I</option>
                <option value='II'>II</option>
                <option value='III'>III</option>
                <option value='IV'>IV</option>
            </select>
            <select style="margin-top: 5px" v-model="block" title="">
                <option value='' selected>Select Block</option>
                <option value='- A'>A</option>
                <option value='- B'>B</option>
                <option value='- C'>C</option>
                <option value='- D'>D</option>
            </select>

            <div style="text-align:center">
                <h5>Result:</h5>
                <h5>{{ firstname }} {{ middlename }} {{ lastname }}</h5>
                <h5>{{ course }} {{ yearlevel }} {{ block }}</h5>

                <h5 style="color: green" v-if="yearlevel == 'IV' ">Congratulations! You are a graduating student.</h5>
                <h5 v-else-if="yearlevel == '' ">Please fil up the form.</h5>
                <h5  v-else>You are not a graduating Student.</h5>
            </div>
        </div>
    </div>
</template>
