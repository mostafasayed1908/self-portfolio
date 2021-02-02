<template>
    <div id="services" class="services-wrapper">
        <div class="container">
            <h3>My Services</h3>
            <div class="borderr">
                <div class="border-itself"></div>
            </div>
            <div class="row">
                <Service 
                v-for="service in services" 
                :key="service.id"
                :icon="service.icon"
                :stitle="service.stitle"
                :scontent="service.scontent"
                />
            </div>
        </div>
    </div>
</template>

<script>
import Service     from   '@/components/Service'
export default {
    data() {
        return {
            services: [
            { id: 1, icon: 'fas fa-file-code', stitle: 'Design Trends', scontent: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.' },
            { id: 2, icon: 'fas fa-images', stitle: 'PSD Design', scontent: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.' },
            { id: 3, icon: 'fas fa-info-circle', stitle: 'Customer Support', scontent: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.' },
            { id: 4, icon: 'fab fa-wordpress', stitle: 'Web Development', scontent: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.' },
            { id: 5, icon: 'fas fa-arrows-alt', stitle: 'Fully Responsive', scontent: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.' },
            { id: 6, icon: 'fas fa-rocket', stitle: 'Branding', scontent: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.' },
            ]
        }
    },
    components: {
        Service,
    }
}
</script>

<style scoped> 
.services-wrapper  {
    padding-top: 30px
}
.services-wrapper h3 {
    width: 100%;
    text-align: center;
    color: #646464;
    font-weight: normal;
}
</style>
