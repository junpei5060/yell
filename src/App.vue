<template>
    <div>
        <Header></Header>
        <TextYell></TextYell>
        <MainYell></MainYell>
    </div>
    
</template>

<script>
import TextYell from './components/TextYell';
import MainYell from './components/MainYell';

export default {
    components: {
        TextYell,
        MainYell
    }
}
</script>