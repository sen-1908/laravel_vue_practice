<script setup>
import { Link } from '@inertiajs/inertia-vue3';
import {ref} from 'vue'

const newTitle = ref('');
const newContent = ref('');


</script>

<template>
<p>Inertiaテストです。</p>
<a href="/">aタグ</a>
<br>
<Link href="/">Link</Link>
<br>
<Link :href="route('inertia.index')" >名前付きroot</Link>
<br>
<Link :href="route('inertia.show', {id: 1})" >パラメーターテスト</Link>

<div class="mb-8" ></div>
<input type="text" name="newTitle" v-model="newTitle" />
<input type="text" name="newContent" v-model="newContent" />
<Link as="button" method="post" :href="route('inertia.store') "
    :data= "{
        title: newTitle,
        content:newContent
    }" >DB保存テスト</Link>
</template>