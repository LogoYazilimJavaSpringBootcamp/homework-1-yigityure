1. Java içerisinde JVM(sanal makina) barındırdığı için platform bağımlı değildir.
   Bu sayede Java platforma ihtiyaç duymadan kendi sanal makinası üzerinde gerekli dönüşümleri yapabilir.
   

2. Çoklu kalıtımda, bir sınıf kendisine ait başka sınıflar türetebilir. Ancak Java bunu desteklemez. Java'da bir sınıf sadece bir sınıf türetebilir.
  Bir A sınıfı olsun. A sınıfı eğer B ve C sınıflarını türetirsin. D sınıfı da B ve C sınıflarından türetilsin.
  Eğer A sınıfındaki bir metot, B ve C sınıflarında override edilirse; D sınıfı hangi sınıfın (B veya C) metodununu kullanacağını bilemez ve belirsizlik oluşur.
  Bu durumun önüne geçmek için Java Interface'leri kullanır.
  
  C++ çoklu kalıtım kullanan bir dildir. C++ belirsizliği önlemek için, türetilen sınıfın ebeveny sınıflarının yapıcı metodlarını kendisine verilen sırayla çağırır.
  
  
3. Build tool, kaynak kodlarının çalıştırılabilir bir dosya haline dönüştürülmesini sağlayan araçtır (örneğin .exe).
  Dönüşüm yapılırken gerekli kütüphaneler yüklenir, kaynak kod makina diline derlenir, ardından paketlenir.
  
  Java için kullanılan build toollardan en bilinenleri; Ant, Maven ve Gradle'dır.
  
4. Collections frameworklerinin en önemli özelliği arraylarin aksine eleman sınırlaması olmamasıdır. Bir array tanımlarken aynı anda eleman sayısı da belirtilmelidir.
  Collections frameworkleri bu durumun önüne geçer ve dinamik bir array sunar.
  
  Collections framework -> List, Queue, Set
  Hepsi birer interface'dir.
  
  List 
    List; istenilen herhangi bir tipte dinamik bir liste oluşturulmasını sağlar. Tekrar eden elemanlar olabilir.
    
    List<Integer> list1 = new ArrayList<Integer>();
    List<String> list2 = new LinkedList<String>();
    List<List<String>> list3 = new Vector<List<String>>();
    List<List<Integer>> list4 = new Stack<List<Integer>>();
  
    Implement edilebilecek sınıflar => List -> ArrayList, LinkedList, Vector, Stack
      
      ArrayList
        ArrayList; dinamik bir array oluşturmak için kullanılır. Elemanlar eklenen sırayla tutulur.
        
        ArrayList<String> arrayList = new ArrayList<String>();
        
      LinkedList
        LinkedList; ArrayList'in özelliklerine sahiptir. Elemanları listeye eklerken container oluşturur ve elemanı container'a ekler. Containerlar birbirine bağlanır.
        
        LinkedList<String> linkedList = new LinkedList<String>();
        
      Vector
        Vector; ArrayList'e benzer. Fazladan kendine ait metodları vardır.
        
        Vector<String> vector = new Vector<String>();
        
      Stack
        Stack; Vector sınıfının alt sınıfıdır. Last-in-first-out yapısındadır.
        
        Stack<String> stack = new Stack<String>();
        
  Queue
    Queue; first-in-first-out yapısında bir interface'dir.
      
    Queue<String> queue1 = new PriorityQueue();
    Queue<String> queue2 = new ArrayDeque();
      
    Implement edilebilecek sınıflar => Queue -> PriorityQueue, ArrayDeque
    
      PriorityQueue
        PriorityQueue; önceliğe göre elemanlarınısıralayan bir sınıftır. null değer barındırmaz.
        
        PriorityQueue<String> priorityQueue=new PriorityQueue<String>();
        
      Deque
        Deque; Queue interface'inden türeyen bir interface'dir. Listenin hem başından hem de sonundan işlem yapabilme olanağı sağlar.
        
        Deque deque = new ArrayDeque();
        
      ArrayDeque
        ArrayDeque; Deque interface'ini kullanabilmeyi sağlayan sınıftır.
        
        Deque<String> arrayDeque = new ArrayDeque<String>();
        
  Set
    Set; tekrarlanamayan elemanları içeren listedir. Interface'dir.
    
    Set<String> s1 = new HashSet<String>();
    Set<String> s2 = new LinkedHashSet<String>();
    Set<String> s3 = new TreeSet<String>();
    
    Implement edilebilecek sınıflar => Set -> HashSet, LinkedHashSet, TreeSet
    
        HashSet
          HashSet; depolamak için hash tablosunu kullanır.
          
          HashSet<String> hashSet = new HashSet<String>();
          
        LinkedHashSet
          LinkedHashSet; LinkedList sınıfının Set interface'i ile kullanılmasıdır. Tekrarlayan eleman barındırmaz, null değer almaz.
          
          LinkedHashSet<String> linkedHashSet = new LinkedHashSet<String>();
          
        SortedSet
          SortedSet; Set interface'inden türetilmiştir. Elemanların büyükten küçüğe ya da küçükten büyüğe sıralanması için kullanılır.
          
          SortedSet<String> set = new TreeSet();
          
        TreeSet
          TreeSet; depolamak için ağaç yapısını kullanır. Bu sayede çok daha hızlı arama sonucu sağlar. Elemanlar küçükten büyüğe doğru sıralanır.
          
          
5. Main
   ![image](https://user-images.githubusercontent.com/66094687/173880593-f8fee711-572c-417b-9c28-b3659d6de8c7.png)
   ![image](https://user-images.githubusercontent.com/66094687/173880715-f91b1059-229e-45bf-a495-4da3a533d923.png)
   ![image](https://user-images.githubusercontent.com/66094687/173881068-5f2dbbf4-5232-4dd1-8e46-87588a94693b.png)
   Çıktı
   ![image](https://user-images.githubusercontent.com/66094687/173881358-8b00c390-fcd6-4e13-b23c-18bc01798ec0.png)
   ![image](https://user-images.githubusercontent.com/66094687/173881436-4cfd84d1-a780-466c-9cfa-654cc88aa0c5.png)
   ![image](https://user-images.githubusercontent.com/66094687/173881577-61b550dc-eda2-4ac3-9006-8b991a197664.png)



