# test_task-Anlim_Soft

1.Фрагмент 1 не сработает, а Фрагмент 2 сработает.

Фрагмент 1 использует стрелочную функцию (let doubleNum = (num) => { ... }). В JavaScript, стрелочные функции не имеют hoisting.
Таким образом, при вызове doubleNum(10) в первом фрагменте кода, интерпретатор выдаст ошибку TypeError, говоря, что doubleNum is not a function (функция не существует).

Фрагмент 2 использует обычное функциональное объявление (function doubleNum(num) { ... }). В этом случае функция будет создана на этапе "поднятия" (hoisting), и она будет доступна для вызова из любой строки кода внутри своей области видимости (в данном случае, глобальной области видимости). Поэтому во втором фрагменте кода вызов doubleNum(10) будет работать правильно и выдаст результат.

2.
Для того чтобы не было лишних тегов, необходимо закрыть тег <component-name>.Исправить ошибку синтаксиса в определении переменной count в  data, заменив точку с запятой на запятую.
```
<template>
	<component-name
		v-for="i of count" 
		:key="i"
		v-if="i < 10" 
	></component-name>
</template>

<script>
export default {
	data() {
		return {
			count: 20,
		};
	},
};
</script>
```

3.
```
function convertToObj(array) {
  const result = {};
  for (const item of array) {
    const { id, count } = item;
    result[id] = count;
  }
  return result;
}
```
