<!--<template>
    <div class="mobile-console">
        <div class="container-fluid">
            <table>
                <tr>
                    <td><i class="fa fa-home" aria-hidden="true"></i></td>
                    <td><i class="fa fa-heart" aria-hidden="true"></i></td>
                    <td><i class="fa fa-shopping-bag" aria-hidden="true"></i></td>
                    <td><i class="fa fa-user" aria-hidden="true"></i></td>
                </tr>
            </table>
        </div>
    </div>

</template>

<script>

</script>

<style scoped>
* {
    margin: 0%;
    padding: 0%;
}
.mobile-console {
    /*position: fixed;
    bottom: 0%;*/
    margin-left: -20px;
}
.container-fluid {
    width: 100%;
    margin: 0%;
    background-color: rgb(0, 0, 0);
    border-top-left-radius: 25px;
    border-top-right-radius: 25px;
    /*transform: scale(1.2);*/
    position: fixed;
    bottom: 0%;
}
ul {
    columns: 2;
}
li {
    display: inline-block;
}
table {
    width: 100%;
    /*border: 1px solid gold;*/
    margin: 0%;
}

td {
    text-align: center;
    height: 60px;
    color: #fff;
}

@media screen and (max-width: 425px) {
    .console {
        display: inline-block;
    }
}


</style>-->

<template>
    <div class="mobile-console">
        <div class="icons">
            <div><i class="fa fa-home" aria-hidden="true"></i></div>
            <div><i class="fa fa-heart" aria-hidden="true"></i></div>
            <div><i class="fa fa-shopping-bag" aria-hidden="true"></i></div>
            <div><i class="fa fa-user" aria-hidden="true"></i></div>
        </div>
    </div>
</template>

<script>

</script>

<style scoped>
* {
    margin: 0px;
    padding: 0px;
    box-sizing: border-box;
}

.mobile-console {
    background-color: black;
    color: #fff;
    height: 60px;
    position: fixed;
    bottom: 0px;
    /*top: 0px;*/
    /*width: 100%;*/
    margin-left: -40px;
    border-top-left-radius: 40px;
    border-top-right-radius: 40px;
}
.fa {
    width: 100px;
    /*border: 1px solid rgb(230, 230, 230);*/
    text-align: center;
}
.icons {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 20px;
    /*width: 100%;*/
}
</style>