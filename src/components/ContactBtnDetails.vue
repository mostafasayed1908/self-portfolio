<template>
    <div class="row">
        <div class="col-md-2 icn-wrapper"><i :class="dIcon"></i></div>
        <div class="col-md-10 details-wrapper">
            <div class="row">
                <div class="col-md-12 details-title">{{dTitle}}</div>
                <div class="col-md-12 details-content">{{dContent}}</div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props:[
        'dIcon',
        'dTitle',
        'dContent'
    ]
}
</script>

<style scoped>
.icn-wrapper {
    border-right: 2px solid rgb(182, 182, 182);
    font-size: 50px
}
.details-wrapper {
    padding-top: 10px
}
.details-wrapper .details-title {
    font-weight: bold
}

</style>
