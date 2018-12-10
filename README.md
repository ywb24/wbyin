JS 继承方式
工厂模式: 因为使用用一个接口创建很多对象会产生大量的重复代码,为了解决这个问题，人们就开始使用工厂模式
Person = (hairs, face, eye) => {
  const o = new Object();
  o.hairs = hairs;
  o.face = face;
  o.eye = eye;
  o.say = () => {
    console.log('say something to me');
  };
  return o;
//我们通过 Person(0,1,2)就可以创建一个包含特定信息的Person对象, 以后要生成对象直接执行Person然后给他传参数就好了;
//比如我们要生成10个Person, 很方便很快;
let c = 10;
while( c-- ) {
  console.log(Person(c,c,c))
};

