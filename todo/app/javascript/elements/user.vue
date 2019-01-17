<template>
  <div class="component">
    <p>Ten toi la {{ name }}</p>
    <p>Toi nam nay {{ age }} tuoi</p>
    <hr>
    <div class="row">
      <div class="col-xs-12 col-sm-12 col-12">
        <app-user-detail :age="age" @ageWasUpdated="age = $event"></app-user-detail>
        <button @click="resetAge">Reset tuoi</button>
      </div>
      <div class="col-xs-12 col-sm-12 col-12">
        <app-user-edit :user-age="age" @ageWasEdited="age = $event"></app-user-edit>
      </div>
      <div>
        <base-input v-model="value" @inputChange="value = $event"></base-input>
      </div>
    </div>
    <button @click="test_mixin">Test Mixins</button>
  </div>
</template>

<script>
  import UserDetail from './user_detail.vue';
  import UserEdit from './user_edit.vue';
  import BaseInput from './base_input.vue';

  import { test } from './mixins/test_mixin.js';

  export default {
    mixins: [test],

    data: function () {
      return {
        name: 'Duy',
        age: 23
      };
    },

    props: ['value'],
    components: {
      appUserDetail: UserDetail,
      appUserEdit: UserEdit,
      baseInput: BaseInput
    },

    methods: {
      resetAge() {
        this.age = 23
      }
    }
  };
</script>
