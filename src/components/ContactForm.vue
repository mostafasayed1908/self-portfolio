<template>
    <div id="contact" class="contact-wrapper">
        <div class="container">
            <h3>GET IN TOUCH</h3>
            <div class="borderr">
                <div class="border-itself"></div>
            </div>
            <div class="row">
                <div class="col-md-12 text-center">
                    <h4>Message Me</h4>
                    <form action="">
                        <div class="row">
                        <Input
                        v-for="input in inputs"
                        :key="input.id"
                        :icol="input.icol"
                        :itype="input.itype"
                        :iholder="input.iholder"
                         />
                         <div class="col-md-12 btn-container">
                        <button type="submit" class="btn btn-secondary">Send Message</button>
                         </div>
                        </div>
                    </form>
                </div>

            </div>
        </div>
    </div>
</template>

<script>
import Input from '@/components/Input'
import ContactBtnDetails from '@/components/ContactBtnDetails'

export default {
    components: {
        Input,
        ContactBtnDetails
    },
    data () {
        return {
            inputs: [
                {id:1,icol:'col-md-6',itype:'text',iholder:'Name'},
                {id:2,icol:'col-md-6',itype:'email',iholder:'Email'},
                {id:3,icol:'col-md-12',itype:'text',iholder:'Subject'},
                {id:4,icol:'col-md-12',itype:'text',iholder:'Message'},
            ]
        }
    }
}
</script>

<style scoped>
.contact-wrapper {
    padding-top: 50px
}
.contact-wrapper h3{
    width: 100%;
    text-align: center;
    color: #646464;
    font-weight: normal;
}
.contact-wrapper form {
    width: 100%;
    padding: 20px 0;

}
.btn-container button {
    width: 140px;
}
</style>
