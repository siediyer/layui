# layer.msg
layer.msg('玩命提示中');

layer.msg('的确很重要', {icon: 1});

layer.msg('也可以这样', {
    time: 20000, //20s后自动关闭
    btn: ['明白了', '知道了']
});


信息框-例2
layer.msg('你确定你很帅么？', {
  time: 0 //不自动关闭
  ,btn: ['必须啊', '丑到爆']
  ,yes: function(index){
    layer.close(index);
    layer.msg('雅蠛蝶 O.o', {
      icon: 6
      ,btn: ['嗷','嗷','嗷']
    });
  }
});

layer.msg('玩命卖萌中', function(){
//关闭后的操作
});

//加载层-风格4
layer.msg('加载中', {
  icon: 16
  ,shade: 0.01
});

//默认prompt
layer.prompt(function(val, index){
  layer.msg('得到了'+val);
  layer.close(index);
});

//正上方
layer.msg('灵活运用offset', {
  offset: 't',
  anim: 6
});

# layer.alert
//信息框-例1
layer.alert('见到你真的很高兴', {icon: 6});

# layer.open
layer.open({
    type: 1,
    title: '查看',
    shadeClose: true,
    shade: 0.8,
    content: '<video  autoplay  width="320" height="80" controls><source src="'+voice+'" ></video>'
}); 

# layer.closeAll
(function(){
    Wind.use('layer');

    layer.msg("操作失败", {}, function () {
        layer.closeAll();
    });
})()
