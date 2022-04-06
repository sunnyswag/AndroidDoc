* ArrayMap：使用的内存比 HashMap 要少，但是效率比 HashMap 要低，适合存储小批量的数据，key 为其他任意类型

* ArraySet：使用的内存比 HashSet 要少，但是效率比 HashSet 要低，适合存储小批量的数据

* SparseArray：使用场景，数据量不大，千级以内；key 必须为 int 类型

* SparseLongArray：SparseLongArrays map integers to longs

* Pair：可以理解为元组(直接是 final 的对象值)，可以采取 ArrayList 和 Pair 搭配使用

* Range：用来记录范围对象

* Rational：可以用来记录分子分母的对象

* Size：记录宽高(SizeF，以 Float 的方式进行记录)

* StateSet

  