<template>
    <div>
        Hello {{firstname}} {{lastname}}. You city is {{city}}
    </div>
</template>
<script>
export default{
  props: ['firstname', 'lastname', 'city']
}
</script>
