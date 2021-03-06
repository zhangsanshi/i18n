# Объект JumpListCategory

* `type` String (опиционально) - одно из следующего: 
  * `tasks` - элементы этой категории будут помещены в стандартную категорию `Tasks`. Там может быть только одна такая категория, и она всегда будет отображается в нижней части списка переходов.
  * `frequent` - отображать список файлов, недавно открытых приложением, имя категории и этого элемента устанавливаются в Windows.
  * `recent` - отображать список файлов, недавно открытых приложением, имя категории и этого элемента устанавливаются в Windows. Элементы могут быть добавлены в эту категорию косвенно, используя `app.addRecentDocument(path)`.
  * `custom` - отображать ссылки на задачи или файлы, `name` должно быть установлено приложением.
* `name` String (опиционально) - должно быть установлено, если `type` является `custom`, в противном случае оно должно быть опущено.
* `items` JumpListItem[] (опиционально) - массив [`JumpListItem`](jump-list-item.md) объектов, если `type` является `tasks` или `custom`, в противном случае оно должно быть опущено.

**Примечание:** Если объект `JumpListCategory` не имеет ни `type`, ни `name` свойства, тогда `type` считается `tasks`. Если свойство `name` установлено, но свойство `type` опущено, тогда `type` считается `custom`.