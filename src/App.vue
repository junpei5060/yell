<template>
    <div>
        <Header></Header>
        <TextYell></TextYell>
        <MainYell></MainYell>
        <YellStudent></YellStudent>
        <ServiceYell></ServiceYell>
    </div>
    
</template>

<script>
import TextYell from './components/TextYell';
import MainYell from './components/MainYell';
import ServiceYell from './components/ServiceYell';
import YellStudent from './components/YellStudent';

export default {
    components: {
        TextYell,
        MainYell,
        ServiceYell,
        YellStudent
    }
}
</script>