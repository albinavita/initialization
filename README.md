## Инициализация
**Инициализация переменной** – это присвоение переменной значения и выделение места в памяти, отведенной java процессу, в рамках которого будет выполняться программа. Эта память разделена на несколько областей или зон:
1.	Heap
2.	Stack
3.	Non-heap  
При запуске программы ОС создает и запускает процесс. Для выполнения в JVM создаётся основной поток (Thread). При создании потока ему выделяется свой стэк в памяти. Этот стэк состоит из фрэймов.
Под каждый новый метод выделяется фрейм и добавляется на вершину стека.
Фрейм может содержать ссылки на объекты и примитивные типы.
В зависимости от принадлежности к классу и расположению переменные могут быть:
- локальные переменные;
- переменные экземпляра;
- статические переменные или переменные класса.
**Локальные переменные**
- Локальные переменные объявляются в методах, конструкторах или блоках.  
- Локальные переменные создаются, когда метод, конструктор или блок запускается и уничтожаются после того, как завершиться метод, конструктор или блок.  
- Модификаторы доступа нельзя использовать для локальных переменных.  
- Они являются видимыми только в пределах объявленного метода, конструктора или блока.  
- Локальные переменные реализуются на уровне стека внутри  .
- **В Java не существует для локальных переменных значения по умолчанию**, так что они должны быть объявлены и начальное значение должны быть присвоено перед первым использованием.
Уже при написании кода среда разработки подскажет, что переменную надо проинициализировать.
  []()
**Переменные экземпляра**
 Переменные экземпляра по другому называются полями.
Чаще всего их объявляют сразу после объявления класса или блока инициализации и имеют модификаторы доступа.
Переменные экземпляра имеют значение по умолчанию:    
-	целочисленные значения - 0;  
-	вещественные значения - 0.0;  
-	логические значения - false;  
-	ссылочные значения - null   
Переменные экземпляра имеют значения по умолчанию. Для чисел по умолчанию равно 0, для логических – false, для ссылок на объект – null. Значения могут быть присвоены при объявлении или в конструкторе.  

‘’’
public class Car {
  // 
    private String color;
    private String brand;

    public Car(String brand) {
        this.brand = brand;
    }

    public void setColor(String color) {
        this.color = color;
    }

    public void print(){
        System.out.println(String.format("%s - %s", brand, color) );
    }

    public static void main(String[] args) {
    
        Car car = new Car("BMW");
        car.setColor("red");
       car.print();
    }
}

‘’’
Вывод на экран
‘’’
BMW - red
‘’’
