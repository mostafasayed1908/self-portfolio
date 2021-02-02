<template>
    <div :class="icol">
        <div class="form-group">
            <input :type="itype" class="form-control"  :placeholder="iholder">
        </div>
    </div>
</template>

<script>
export default {
    props: [
        'icol',
        'itype',
        'iholder']
    
}
</script>

<style scoped>
input {
    border: none;
    border-bottom: solid #d1d1d1 1px;
    border-radius: 0;
    background-color: #fcfcfc;
}
.form-control:focus {
    color: #495057;
    background-color: #fff;
    border-color: #80bdff00;
    outline: 0;
    box-shadow: 0 0 0 .2rem rgba(0, 123, 255, 0);
}
</style>
