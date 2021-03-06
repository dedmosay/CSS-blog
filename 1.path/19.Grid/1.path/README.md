## GRID

# ЧАСТЬ 1

![](https://github.com/dedmosay/CSS-blog/blob/master/1.path/19.Grid/image/grid.jpg)

### Transition

- ```Grid-inline``` - Линии.
Можно ссылаться по числовому индексу.
- ```Grid-trap``` - Дорожки сетки.
Дорожка занимает либо всю ширину, либо все высоту контейнера.
По умолчанию все дорожки прилегают друг другу.

- ```Grid-ceil``` - Ячейка сетки.
Пространство ограничивается четырьмя линиями. Внутрь ячейки можно помещать контент.
К ячеке нельзя обращаться на прямую с помошью css свойств.

- ```Grid-area``` - Область сетки. 
Прямоугольная область, состоящая из 1 либо несколько ячеек.
По умолчанию на нее ссылаются ограничивающие линии сетки.
- ```Grid-items``` - Объекты котрой назначаются области ячейки сетки.
Каждый контейнер может содержать от 0 до infinity grid-элементов. Каждый дочерний элемент grid-контенера автоматически становится grid-элементом.

### Grid контейнер  - ```display:grid``` или ```display:inline-grid ```

Занимает всю ширину.
```css
.grid {
  display: grid;
  font-size: 30px;
}
```
Занимает ширину текста.
```scss
.inline-grid {
  display:inline-grid;
} 
```
![](https://github.com/dedmosay/CSS-blog/blob/master/1.path/19.Grid/image/grid-column-row.jpg)
```scss
display: grid;
grid-auto-rows:200px 100px; // 2 строки
grid-template-columns: 200px  150px 300px; // 3 колонки 
```
![](https://github.com/dedmosay/CSS-blog/blob/master/1.path/19.Grid/image/grid-column-row-fr.jpg)

- ед.изм. в % и fr
```scss
grid-auto-rows: 50%  50%   ; // 2 строки 50%
grid-template-columns: 2fr  1fr 2fr; // 3 колонки  fr 1 1 1 === 33.333%
```

- minmax
![](https://github.com/dedmosay/CSS-blog/blob/master/1.path/19.Grid/image/minmax(auto).gif)
```scss
display: grid;  
grid-template-columns: 300px minmax(200px, 600px) 300px; // minmax(min, max) 3 колонки
grid-template-rows: 1fr  1fr; // 2 строки
```
- fit-content

Ограничение ширины 100px в первой колонке.

![](https://github.com/dedmosay/CSS-blog/blob/master/1.path/19.Grid/image/fit-content.jpg)


```scss
    display: grid;  
    grid-template-columns: fit-content(100px) 1fr 1fr; // 3 колонки 
    grid-template-rows: 1fr  1fr; // 2 строки
```

- Оптимизация записи

```repeat(3, 1fr );``` равнозначено записи  ```1fr 1fr 1fr;```

```scss
grid-template-columns: repeat(3, 1fr ); // 3 колонки 
grid-template-rows: repeat(2, 100px); // 2 строки
```

- Имена областей ```areas```

```scss
.grid {
  &-wrapper {
    display: grid;
    grid-template-columns: 150px 1fr; // 2е колонки
    grid-template-rows: 100px 1fr;    // 2е строки
    grid-template-areas:  
      "header header"           //     header 
      "side content"            // side     content
    ;
  }
  &-header,&-side,&-content { 
    text-align: center;  
    border: 2px dashed #aaa;
    padding: 30px;
    margin: 10px 0;
  }
  &-header {
    grid-area: header;
  }
  &-side {
    grid-area: side;
  }
  &-content {
    grid-area: content;
  }
}
```
До и после приминения ```area```
![](https://github.com/dedmosay/CSS-blog/blob/master/1.path/19.Grid/image/area.jpg)

 - grid-template
 СТРОКИ / КОЛОНКИ
```
repeat(<количество>, __px) /  repeat(количество, __px )
```
 ```scss
     display: grid;  

    grid-template:  repeat(2, 100px) /  repeat(3, 1fr );  // РЯДЫ / КОЛОНКИ

    // grid-template-columns: repeat(3, 1fr ); // 3 колонки 
    // grid-template-rows: repeat(2, 100px); // 2 строки
  ```

ИМЕНА ОБЛАСТЕЙ
```
[start] "<name1> <name1>" __px [row2]
[start] "<name3> <name4>" __px [row-end] / __px __px
```

```scss
    grid-template: 
      [start] "header header" 100px [row2]              //   строки 100px.  [row2]  - конец и начало.
      [row2] "side content" 1fr [row-end] / 150px 1fr;  //  [row2] "side content" 1fr [row-end] / 150px 1fr;  

    // grid-template-areas: 
    //   "header header" 
    //   "side content"
    // ;
```

- Неявная сетка

![](https://github.com/dedmosay/CSS-blog/blob/master/1.path/19.Grid/image/grids.jpg)

Для управления 7й ячейки необходимо использовать ```grid-auto-rows: __px``` и ```grid-auto-columns: __px``` 


- Автоматическое размещение

![](https://github.com/dedmosay/CSS-blog/blob/master/1.path/19.Grid/image/auto.jpg)
