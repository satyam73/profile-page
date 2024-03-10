<script lang='ts'>
  export let image: string;
  export let text: string;
  export let link: string = 'https://google.com';
</script>

<a href={link} target="_blank">
  <div class="w-[344px] h-[226px] border rounded-xl overflow-hidden">
    <img class="object-cover w-full h-[136px]" src={image} alt="">
    <div class="h-[90px] flex items-center px-3 text-[#141618] text-sm font-normal">
      <div class="h-[41px] line-clamp-2">
        {text}
      </div>
    </div>
  </div>
</a>