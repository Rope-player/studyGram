<template>
    <v-row>
        <v-col cols="" sm="6" class="my-2 px-1">
            <v-date-picker 
                ref="picker"
                v-model="date"
                :picker-date.sync="pickerDate"
                full-width
                ></v-date-picker>
        </v-col>
        <v-col cols="12" sm="6" class="my-2 px-1">
        <div class="title">이달의 행사 ({{ pickerDate || 'change month...' }})</div>
        <div class="subheading">다른 일정을 보기위해서 월을 변경하세요.</div>
        <ul class="ma-4">
            <li v-for="note in notes" :key="note">{{ note }}</li>
        </ul>
        </v-col>
    </v-row>
</template>

<script>
  export default {
    data: () => ({
      date: new Date().toISOString().substr(0, 10),
      pickerDate: null,
      notes: [],
      allNotes: [
        '일정1',
        '일정2',
        '일정3',
        '일정4',
        '일정5',
      ],
    }),
    watch: {
      pickerDate (val) {
        this.notes = [
          this.allNotes[Math.floor(Math.random() * 5)],
          this.allNotes[Math.floor(Math.random() * 5)],
          this.allNotes[Math.floor(Math.random() * 5)],
        ].filter((value, index, self) => self.indexOf(value) === index)
      },
    },
  }
</script>