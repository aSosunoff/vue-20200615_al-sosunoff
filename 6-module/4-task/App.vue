<template>
  <div id="app" class="wrapper bg-grey page">
    <div class="container">
      <pre><code>{{ agendaItem }}</code></pre>
      <meetup-agenda-item-form
        :agenda-item="agendaItem"
        @remove="handleRemove"
      />
    </div>
  </div>
</template>

<script>
import MeetupAgendaItemForm from './components/MeetupAgendaItemForm';

export default {
  name: 'App',

  components: { MeetupAgendaItemForm },

  data() {
    return {
      agendaItem: {
        /* id: 0,
        startsAt: '00:00',
        endsAt: '00:00',
        type: 'other',
        title: null,
        description: null,
        speaker: null,
        language: null, */

        id: 0,
        startsAt: '05:00',
        endsAt: '10:00',
        type: 'other',
        title: 'Title',
        description: 'Description',
        speaker: null,
        language: null,
      },
    };
  },

  methods: {
    handleRemove() {
      alert('removed');
    },
  },
};
</script>

<style></style>
