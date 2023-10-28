<template>
    <DynamicProp>
        Your {{fullName}}
    </DynamicProp>
</template>
<script>
export default{
  props: ['fullName']
}
</script>
