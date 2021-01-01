<script>
  export let item;
</script>

<div class="m-3 p-3 shadow rounded">
  <h3 class="text-center">{item.timestamp}</h3>
  <div class="py-6 flex justify-around">
    <div class="p-2">
      <i class="fas fa-thermometer-half text-blue-400" />
      {item.temperatura}
    </div>
    <div class="p-2">spO² - {item.oxigenación}%</div>
    <div class="p-2">
      <i class="fas fa-heartbeat text-red-500" />
      {item.sistólica}/{item.diastólica}
    </div>
  </div>
</div>
