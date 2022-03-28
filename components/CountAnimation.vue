<template>
    <div>
    <amp-script width="200" height="100" script="hello-world">
    <button>Hello amp-script!</button>
    </amp-script>
    </div>
</template>

<script id="hello-world" type="text/plain" target="amp-script">
  const btn = document.querySelector('button');
  btn.addEventListener('click', () => {
    document.body.textContent = 'Hello World!';
  });
</script>

<script>
export default {
    
}
</script>
