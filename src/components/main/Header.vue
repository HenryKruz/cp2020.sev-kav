<template>
    <div>
        <div class='header-container'>
            <div class="header-logo">
                <img src="/static/img/logo.png" width="100px" height="auto">
            </div>
            <div class="header-user-panel">
                <span class="header-user-name"><strong>{{ userName }}</strong></span>
                <img src="/static/img/person.png" width="auto" height="30px">
                <ul>
                    <li v-on:click="logout">Выход</li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'app-header',
    data() {
        return {
            userName: sessionStorage.getItem('userName')
        }
    },
    methods: {
        logout() {
            sessionStorage.removeItem('sessionId');
            this.$router.push({name: 'Login'});
        }
    }
}
</script>

<style scoped>
.header-container {
    padding: 0 20px;
    height: 60px;
    box-shadow: 0 1px 10px 0px grey;
}
.header-logo {
    display: inline-block;
    float: left;
}
.header-user-panel {
    float: right;
}

.header-user-panel img{
    margin: 12px 0;
}
.header-user-panel ul {
    display: none;
    list-style: none;
}
.header-user-panel ul li {
    cursor: pointer;
}
.header-user-panel:hover ul {
    display: block;
    margin: 0;
}
.header-user-name {
    padding-right: 15px;
}
</style>