<template>
    <div class="tools">
        <UserAccount v-if="user" />
        <UserLogin :isDesktop="isDesktop" v-else/>
    </div>
</template>

<script>
import UserAccount from '@/components/header/icon-account';
import UserLogin from '@/components/header/icon-login';

export default {
    components: {
        UserAccount,
        UserLogin
    }, 
    props: {
        isDesktop: Boolean
    },
    data() {
        return {
            user: true
        }
    }
}
</script>