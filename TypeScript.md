# Стандарты кодирования — TypeScript

### Форматирование
Для отступов используем табуляцию.
Для фигурных скобок испольузем K&R стиль:
```
interface Foo {
    bar: string;
}
```

##### Длина строки
- Максимальная допустимая длина строки — 130 символов
- Символ табуляция считается за 4 символа
- Пробельные символы в конце строки учитываются

### Именование
- Имена экспортируемых классов и переменных должны быть уникальны
- Имя файла соответствует имени класса. В случае с React - имени компонента.
- Компоненты-контейнеры не имеют постфикса.
- Компоненты-рисовашки имеют постфикс Presenter

### Деление React-компонентов на файлы
##### Минимальный вариант
- MyComponent - контейнер
- MyComponentPresenter - презентер
- MyComponentReducer - Reducer, Actions, Action Creators
##### Средний вариант
- MyComponent - контейнер
- MyComponentPresenter - презентер
- MyComponentReducer - Reducer, Action Creators
- MyComponentActions - Actions
##### Максимальный вариант
- MyComponent - контейнер
- MyComponentPresenter - презентер
- MyComponentReducer - Reducer
- MyComponentActionCreators - Action Creators
- MyComponentActions - Actions

### Папки
Группируем файлы по папкам соответственно функционалу, а не архитектурным срезам. Пример:
- Operation
  - OperationSteps
    - AddOrEditOperationStep
		-	AddOrEditOperationStep.ts
		-	AddOrEditOperationStepPresenter.tsx
		-	AddOrEditOperationStepReducer.ts
	-	SendEmailOperationStep
        - …
    - OutptutWriters
	    - CustomerOutputWriter
	    	- ...
