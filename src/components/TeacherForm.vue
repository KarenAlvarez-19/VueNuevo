<template>
  <section>
    <h3>Añadir profesor</h3>
    <div>
        <label>Nombre:</label>
        <input type="text" v-model="teacher.teacherName"/>
    </div>

    <div>
        <label>Apellidos:</label>
        <input type="text" v-model="teacher.surname"/>
    </div>

    <div>
        <label>DNI / NIF:</label>
        <input type="text" v-model="teacher.dni"/>
    </div>
    <div>
        <label>Materias:</label>
        <input type="text" v-model="subject"/>
        <button  @click="handleSubjects()">Agregar</button>
    </div>

    <div>
      |<ul>
      <li v-for="(elm, index) in teacher.subjects" :key="index">{{ elm }}</li>
      </ul>
    </div>

    <input type="checkbox" v-model="teacher.doc"/> Documentación entregada
    <button @click="handleAddTeachers()">Agregar</button>
  </section>

  <section>
    <h3>Listado de profesores</h3>
      <table>
        <tr>
          <th>Nombre | </th>
          <th>Apellidos | </th>
          <th>DNI / NIF | </th>
          <th>Materias | </th>
          <th>Documentación entregadaaaa |</th>
        </tr>
        <tr v-for="elm in teachers" :key="elm.dni">
        <th>{{ elm.teacherName }}</th>
        <th>{{ elm.surname }}</th>
        <th>{{ elm.dni }}</th>
        <th>{{ elm.teacherName }}</th>
        <th>
          <ul>
            <li v-for="(item, index) in elm.subjects" :key="index">{{ item }}</li>
          </ul>
        </th>
        <th v-if="elm.doc">Entregada</th>
        <th v-if="elm.doc">No Entregada</th>
      </tr>
      </table>
  </section>
</template>

<script lang="ts" setup>
    import {Ref, ref} from 'vue';

    interface ITeacher{ //tipando los datos
      teacherName: string,
      surname:string,
      dni:string,
      subjects:Array<string>,
      doc: boolean  

    }

    let teacher:Ref<ITeacher> = ref({
        teacherName: '',
        surname: '',
        dni: '',
        subjects:[],
        doc: false
    })

    let teachers:Ref<Array<ITeacher>> = ref([]) //Array en donde se guardara la info

    let subject:Ref<string> = ref('') //aqui se guardan las materias

      //esta función es para inserta la información del subject dentro del objeto teacer 
      const handleSubjects = () => {
        teacher.value.subjects.push(subject.value)
        subject.value= ""
      }

      const handleAddTeachers = () => {
        teachers.value.push(teacher.value)
        teacher.value.teacherName= ""
        teacher.value.surname= ""
        teacher.value.dni= ""
        teacher.value.subjects= []
        teacher.value.doc= false
      }
</script>

<style scoped>
</style>