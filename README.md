# cityData 统计局最新省市区联动数据
数据截止 2013年8月31日
http://www.stats.gov.cn/tjsj/tjbz/xzqhdm/201401/t20140116_501070.html

# Usage
- citydata.txt 省市区数据列表
- location.js 联动组件DEMO

```html
<div id="select">
    <select name="prov"></select>
    <select name="city"></select>
    <select name="dist"></select>
</div>

<script>
$(document).ready(function(){
    var demo = $('#select').location(110101);
    $('#getregion').click(function(){
        var id   = demo.getRegionId();
        var data = demo.id2Region(id);
        $('#info').html('编号: '+id+'<br> 位置: '+data.region.join(' '));
    });
});
</script>
```
