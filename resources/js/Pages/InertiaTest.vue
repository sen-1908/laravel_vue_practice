<script setup>
import { Link } from '@inertiajs/inertia-vue3';
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
</template>