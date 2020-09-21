# Лабораторная работа №1. Layouts
## Цели
* Ознакомиться со средой разработки Android Studio;
* Изучить основные принципы верстки layout с использованием View и ViewGroup;
* Изучить основные возможности и свойства LinearLayout;
* Изучить основные возможности и свойства ConstraintLayout;

## Задачи
### Задача 1.  LinearLayout
#### Задание
Создать layout ресурсы для следующих макетов экрана с использованием LinearLayout. Макеты соответствуют 8 варианту.

Изображение 1: 

![Иллюстрация к проекту](https://github.com/stalnoi0edinorog/androidLab1/blob/master/forReport/1.png)

Изображение 2: 

![Иллюстрация к проекту](https://github.com/stalnoi0edinorog/androidLab1/blob/master/forReport/2.png)

Созданные layout ресурсы для макета экрана 1 с использованием LinearLayout:

![Иллюстрация к проекту](https://github.com/stalnoi0edinorog/androidLab1/blob/master/forReport/layoutTask1_1.JPG)

Созданные layout ресурсы для макета экрана 2 с использованием LinearLayout:

![Иллюстрация к проекту](https://github.com/stalnoi0edinorog/androidLab1/blob/master/forReport/layoutTask1_2_1.JPG)

**LinearLayout** – макет, выравнивающий все дочерние объекты в одном направлении — вертикально или горизонтально.Все дочерние элементы LinearLayout располагаются друг за другом, поэтому в вертикальном списке будет только один дочерний элемент для каждой строки, независимо от того, насколько они широки, а горизонтальный список будет иметь высоту только в одну строку (высота самого высокого дочернего элемента плюс отступ).

**layout_weight** – атрибут, определяющий "важность" представления и позволяющий элементу расширяться, чтобы заполнить любое оставшееся пространство в родительском представлении.

**gravity** – атрибут, задающий позиционирование содержимого элемента.

**layout_gravity** - позиционирование содержимого относительно родителя.

**orientation** – атрибут, задающий направление: "horizontal" или "vertical".

**layout_height, layout_width** – атрибуты, определяющие размер высоты и ширины.  Для них существуют const: match_parent (представление должно быть таким же большим, как его родитель (за исключением заполнения)), wrap_content (представление должно быть достаточно большим, чтобы вместить его содержимое (плюс отступы)). 

Решение задачи для макета экрана 2 с использованием элемента space и нескольких linearLayout:

![Иллюстрация к проекту](https://github.com/stalnoi0edinorog/androidLab1/blob/master/forReport/layoutTask1_2_2.JPG)

Элемент space используют для создания промежутков между компонентами в макетах.

### Задача 2. ConstraintLayout
#### Задание
Решите задачу 1 (обе подзадачи) с использованием ConstraintLayout.
Созданные layout ресурсы для макета экрана 1 с использованием ConstraintLayout:

![Иллюстрация к проекту](https://github.com/stalnoi0edinorog/androidLab1/blob/master/forReport/layoutTask2_1.JPG)

Созданные layout ресурсы для макета экрана 2 с использованием ConstraintLayout:

![Иллюстрация к проекту](https://github.com/stalnoi0edinorog/androidLab1/blob/master/forReport/layoutTask2_2.JPG)

**ConstraintLayout** - это android.view.ViewGroup, которая позволяет гибко размещать и изменять размеры виджетов.

**ConstraintLayout** позволяет создавать большие и сложные макеты с плоской иерархией представлений. Все возможности ConstraintLayoutдоступны непосредственно из визуальных инструментов редактора макета. 

**layout_constraintDimensionRatio** – используя это ограничение макета, мы можем определить одно измерение вида (высота или ширина) как отношение другого измерения.

**layout_constraintHorizontal_weight, layout_constraintVertical_weight** - работают также, как и layout_weight в LinearLayout. Таким образом, представление с наибольшим значением веса получает наибольшее количество места; представления с одинаковым весом занимают одинаковое количество места.

### Задача 3. ConstraintLayout
Создайте layout ресурс для следующего макета экрана с использованием ConstraintLayout.

Изображение 3:

![Иллюстрация к проекту](https://github.com/stalnoi0edinorog/androidLab1/blob/master/forReport/3.png)

Созданные layout ресурсы для макета экрана 3 с использованием ConstraintLayout:

![Иллюстрация к проекту](https://github.com/stalnoi0edinorog/androidLab1/blob/master/forReport/layoutTask3.JPG)

**Guideline** - вспомогательные объекты, не отображающиеся на устройстве и использующиеся только для целей компоновки макета. Они работают только внутри ConstraintLayout.
В данном задании использование guideline позволяет разделить макет в нужных пропорциях, а затем ограничить ими позиции компонентов.

## Выводы
В процессе выполнения лабораторной работы в среде разработки AndroidStudio были изучены основы верстки layout с использованием View (элеметны интерфейса) и ViewGroup (может содержать дугие View). Также были изучены основные возможности и свойства LinearLayout и ConstraintLayout. Для строгого представления элементов можно использовать LinearLayout, а для сложной верстки, где может понадобиться «привязывание» элементов друг к другу или родителям, необходимо использовать ConstraintLayout. Также в LinearLayout для уменьшения объёма кода и удобства чтения повторяющиеся кострукции были вынесены с style.xml.

### Приложения
#### Содержание файла task1_1.xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView2"
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:text="@string/txt"
        style="@style/forText" />

    <Button
        android:id="@+id/button4"
        android:layout_width="match_parent"
        android:layout_height="50dp"
        android:text="@string/cat" />

    <ImageView
        android:id="@+id/imageView6"
        android:layout_width="match_parent"
        android:layout_height="50dp"
        app:srcCompat="@drawable/cat" />

</LinearLayout>

#### Содержание файла task1_2_1.xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical">

    <Button
        android:id="@+id/button"
        android:layout_width="137dp"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:layout_gravity="start"
        android:text="@string/cat" />

    <TextView
        android:id="@+id/textView"
        android:layout_width="137dp"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:layout_gravity="center"
        android:text="@string/summer"
        style="@style/forText" />

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="137dp"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:layout_gravity="end"
        app:srcCompat="@drawable/catm" />

</LinearLayout>

#### Содержание файла task1_2_2.xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:orientation="horizontal">

        <Button
            android:id="@+id/button3"
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:text="@string/cat" />

        <Space
            style="@style/forSpace" />

        <Space
            style="@style/forSpace" />
    </LinearLayout>

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:orientation="horizontal">

        <Space
            style="@style/forSpace" />

        <TextView
            android:id="@+id/textView4"
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:text="@string/summer"
            style="@style/forText" />

        <Space
            style="@style/forSpace" />
    </LinearLayout>

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:orientation="horizontal">

        <Space
            style="@style/forSpace" />

        <Space
            style="@style/forSpace" />

        <ImageView
            android:id="@+id/imageView3"
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="1"
            app:srcCompat="@drawable/catm" />
    </LinearLayout>

</LinearLayout>

#### Содержание файла task2_1.xml

<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/linearLayout"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView2"
        style="@style/forText"
        android:layout_width="wrap_content"
        android:layout_height="0dp"
        android:text="@string/txt"
        app:layout_constraintBottom_toTopOf="@+id/button4"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/button4"
        android:layout_width="0dp"
        android:layout_height="50dp"
        android:text="@string/cat"
        app:layout_constraintBottom_toTopOf="@+id/imageView6"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView2" />

    <ImageView
        android:id="@+id/imageView6"
        android:layout_width="0dp"
        android:layout_height="50dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/button4"
        app:srcCompat="@drawable/cat" />

</androidx.constraintlayout.widget.ConstraintLayout>

#### Содержание файла task2_2.xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/linearLayout2"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <androidx.constraintlayout.widget.Guideline
        android:id="@+id/guideline1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:orientation="horizontal"
        app:layout_constraintGuide_percent="0.33"/>

    <androidx.constraintlayout.widget.Guideline
        android:id="@+id/guideline2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:orientation="horizontal"
        app:layout_constraintGuide_percent="0.66"/>

    <Button
        android:id="@+id/button"
        android:layout_width="0dp"
        android:layout_height="0dp"
        android:text="@string/cat"
        app:layout_constraintBottom_toTopOf="@+id/guideline1"
        app:layout_constraintEnd_toStartOf="@+id/textView"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <TextView
        android:id="@+id/textView"
        style="@style/forText"
        android:layout_width="wrap_content"
        android:layout_height="0dp"
        android:text="@string/summer"
        app:layout_constraintBottom_toTopOf="@+id/guideline2"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="@+id/guideline1" />

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="0dp"
        android:layout_height="0dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toEndOf="@+id/textView"
        app:layout_constraintTop_toTopOf="@+id/guideline2"
        app:srcCompat="@drawable/catm" />

</androidx.constraintlayout.widget.ConstraintLayout>

#### Содержание файла task3.xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <androidx.constraintlayout.widget.ConstraintLayout
        android:layout_width="match_parent"
        android:layout_height="0dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintDimensionRatio="1:1"
        app:layout_constraintTop_toTopOf="parent"
        tools:layout_editor_absoluteX="0dp">


        <androidx.constraintlayout.widget.Guideline
            android:id="@+id/line1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:orientation="vertical"
            app:layout_constraintGuide_percent="0.2" />

        <androidx.constraintlayout.widget.Guideline
            android:id="@+id/line2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:orientation="vertical"
            app:layout_constraintGuide_percent="0.4" />

        <androidx.constraintlayout.widget.Guideline
            android:id="@+id/line3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:orientation="vertical"
            app:layout_constraintGuide_percent="0.6" />

        <androidx.constraintlayout.widget.Guideline
            android:id="@+id/line4"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:orientation="vertical"
            app:layout_constraintGuide_percent="0.8" />

        <androidx.constraintlayout.widget.Guideline
            android:id="@+id/line5"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            app:layout_constraintGuide_percent="0.2" />

        <androidx.constraintlayout.widget.Guideline
            android:id="@+id/line6"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            app:layout_constraintGuide_percent="0.4" />

        <androidx.constraintlayout.widget.Guideline
            android:id="@+id/line7"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            app:layout_constraintGuide_percent="0.6" />

        <androidx.constraintlayout.widget.Guideline
            android:id="@+id/line8"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            app:layout_constraintGuide_percent="0.8" />

        <ImageView
            android:id="@+id/imageView2"
            android:layout_width="0dp"
            android:layout_height="0dp"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintEnd_toStartOf="@+id/line3"
            app:layout_constraintStart_toStartOf="@+id/line1"
            app:layout_constraintTop_toTopOf="@+id/line8"
            app:srcCompat="@drawable/catm" />

        <ImageButton
            android:id="@+id/imageButton"
            android:layout_width="0dp"
            android:layout_height="0dp"
            app:layout_constraintBottom_toTopOf="@+id/line8"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="@+id/line4"
            app:layout_constraintTop_toTopOf="@+id/line6"
            app:srcCompat="@drawable/cat1" />

        <TextView
            android:id="@+id/textView3"
            style="@style/forText"
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:text="@string/cat2"
            app:layout_constraintBottom_toTopOf="@+id/line8"
            app:layout_constraintEnd_toStartOf="@+id/line4"
            app:layout_constraintStart_toStartOf="@+id/line2"
            app:layout_constraintTop_toTopOf="@+id/line7" />

        <ToggleButton
            android:id="@+id/toggleButton"
            android:layout_width="0dp"
            android:layout_height="0dp"
            app:layout_constraintBottom_toTopOf="@+id/line5"
            app:layout_constraintEnd_toStartOf="@+id/line2"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toTopOf="parent"/>

        <RatingBar
            android:id="@+id/ratingBar2"
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:numStars="3"
            app:layout_constraintBottom_toTopOf="@+id/line6"
            app:layout_constraintEnd_toStartOf="@+id/line2"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toTopOf="@+id/line5" />

        <CheckBox
            android:id="@+id/checkBox"
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:text="@string/click"
            app:layout_constraintBottom_toTopOf="@+id/line6"
            app:layout_constraintEnd_toStartOf="@+id/line4"
            app:layout_constraintStart_toStartOf="@+id/line3"
            app:layout_constraintTop_toTopOf="parent" />

    </androidx.constraintlayout.widget.ConstraintLayout>

</androidx.constraintlayout.widget.ConstraintLayout>
