
<template>
  <div>
    <b-form @submit="onSubmit" @reset="onReset" v-if="show">
      <b-form-group id="input-group-1" label="Краткое содержание:" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form.short_desc"
          placeholder="Краткое содержание"
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-2" label="Полное содержание" label-for="input-2">
        <b-form-textarea
          id="input-2"
          v-model="form.long_desc"
          placeholder="Полное содержание"
          required
        ></b-form-textarea>
      </b-form-group>

      <b-form-group id="input-group-4" v-slot="{ ariaDescribedby }">
        <b-form-checkbox
          v-model="form.sale"
          id="checkboxes-4"
          :aria-describedby="ariaDescribedby"
          value="yes"
          unchecked-value="no"
        >Применять скидку
        </b-form-checkbox>
      </b-form-group>

      <!-- <b-form-group id="input-group-3" label="Food:" label-for="input-3">
        <b-form-select
          id="input-3"
          v-model="form.food"
          :options="foods"
          required
        ></b-form-select>
      </b-form-group> -->

      <p><b>Параметры</b></p>
      <b-form-group id="input-group-1" label="Серия:" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form.series"
          placeholder="Краткое содержание"
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-2" label="Количество страниц" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form.page_num"
          placeholder="Полное содержание"
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-3" label="Переплет" label-for="input-3">
        <b-form-select
          id="input-3"
          v-model="form.pereplet"
          :options="pereplet"
          required
        ></b-form-select>
      </b-form-group>

      <b-form-group id="input-group-2" label="Автор" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form.author"
          placeholder="Автор"
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-2" label="Год выпуска" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form.year"
          placeholder="Год выпуска"
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-2" label="ISBN" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form.isbn"
          placeholder="ISBN"
          required
        ></b-form-input>
      </b-form-group>

      <p><b>Дополнительные поля</b></p>
      <b-form-group label="PDF:" label-cols-sm="2" label-size="sm">
        <b-form-file id="file-small" size="sm"></b-form-file>
      </b-form-group>

      <b-form-group label="Аудио книга:" label-cols-sm="2" label-size="sm">
        <b-form-file id="file-small" size="sm"></b-form-file>
      </b-form-group>

      <p><b>НДС</b></p>
      <b-form-group id="input-group-2" label="НДС" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form.nds"
          placeholder="НДС"
          required
        ></b-form-input>
      </b-form-group>
      <b-button type="submit" variant="primary">Добавить</b-button>
      <!-- <b-button type="reset" variant="danger">Reset</b-button> -->
    </b-form>
    <!-- <b-card class="mt-3" header="Form Data Result">
      <pre class="m-0">{{ form }}</pre>
    </b-card> -->

    
  </div>
</template>

<script>
  export default {
    data() {
      return {
        form: {
          email: '',
          name: '',
          food: null,
          checked: []
        },
        pereplet: [{ text: 'Select One', value: null }, 'Твердый', 'Мягкий', 'Еще третий тип'],
        show: true
      }
    },
    methods: {
      onSubmit(event) {
        event.preventDefault()
        alert(JSON.stringify(this.form))
      },
      onReset(event) {
        event.preventDefault()
        // Reset our form values
        this.form.email = ''
        this.form.name = ''
        this.form.food = null
        this.form.checked = []
        // Trick to reset/clear native browser form validation state
        this.show = false
        this.$nextTick(() => {
          this.show = true
        })
      }
    }
  }
</script>
