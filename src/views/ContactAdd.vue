<template>
    <div>
        <h4>Thêm mới liên hệ</h4>
            <ContactForm 
                :contact='{}'
                @contact-submit='addContact'
            />
        <p>{{message}}</p>
    </div>
</template>

<script>
import ContactForm from '../components/ContactForm.vue'
import ContactService from '../services/contact.service'

export default {
    name: 'ContactAdd',
    components: {
        ContactForm,
    },
    data(){
        return {
            message: '',
        }
    },
    methods: {
        async addContact(data){
            const [error, response] = await this.handle(ContactService.create(data))

            if(error){
                console.log(error)
            }else{
                console.log(response.data)
                this.message = 'Đã thêm thành công'
            }
            console.log(data)
            
        }
    }
}
</script>

<style>

</style>