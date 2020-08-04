## flex


```css
    display: flex;
```
- По умолчанию 

![](https://github.com/dedmosay/CSS-blog/blob/master/1.path/16.FLEXBOX/image/flex%20full.jpg)
- Поведение при изменении размера эрана 

![](https://github.com/dedmosay/CSS-blog/blob/master/1.path/16.FLEXBOX/image/flex.jpg)

## inline-flex

```css
    display: inline-flex;
```

- По умолчанию 

![](https://github.com/dedmosay/CSS-blog/blob/master/1.path/16.FLEXBOX/image/inline-flex%20full.jpg)
- Поведение при изменении размера эрана 

![](https://github.com/dedmosay/CSS-blog/blob/master/1.path/16.FLEXBOX/image/inline-flex.jpg)

## justify-content

```justify-content``` - определяет выравнивание вдоль основной оси и принимает один из параметров:
- ```flex-start``` разместить все блоки с права.
- ```flex-end``` разместить все блоки слева.
- ```center``` разместить все блоки по центру.
- ```space-between``` пространство между блоками.
- ```space-around``` пространство со всех сторон

```css
    display: flex;
    justify-content: flex-end;
```

- По умолчанию 

![](https://github.com/dedmosay/CSS-blog/blob/master/1.path/16.FLEXBOX/image/justify-content%20full.jpg)
- Поведение при изменении размера эрана

![](https://github.com/dedmosay/CSS-blog/blob/master/1.path/16.FLEXBOX/image/justify-content.jpg)
## align-items

```align-items``` определяет поведение вдоль поперечной оси.

- ```stretch``` значение по умолчанию.
- ```flex-start``` выранивание по высоте начало сверху.
- ```flex-end``` выранивание по высоте начало снизу.
- ```center``` выранивание по высоте по центру.
- ```baseline``` выранивание по высоте базовой линии шрифта.

```css
    display: flex;
    align-items: flex-start;
```

## flex-wrap

- По умолчанию 

![](https://github.com/dedmosay/CSS-blog/blob/master/1.path/16.FLEXBOX/image/flex-wrap%20full.jpg)
- Поведение при изменении размера эрана 

![](https://github.com/dedmosay/CSS-blog/blob/master/1.path/16.FLEXBOX/image/flex-wrap.jpg)

- Переворот значений 

![](https://github.com/dedmosay/CSS-blog/blob/master/1.path/16.FLEXBOX/image/flex-wrap-reverse.jpg)
```css
    display: flex;
    flex-wrap: wrap;
```
