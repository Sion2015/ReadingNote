## Python Data Model:

* _Start date: 6/7/2019, Finished at 6/7/2019_
* Official Doc: https://docs.python.org/3/reference/datamodel.html

1.  \_\_getitems\_\_:
    * make class be iterable and support slicing

2. Different between \_\_repr\_\_ and \_\_str\_\_
    * \_\_repr\_\_: Choose when you only need to implement one of thses two method. 
      * Use for unambiguous
    * \_\_str\_\_: called by str(), shoud be suitable for display to end users.     
      * Use for readable
    * if \_\_str\_\_ is not implemented, Python will call \_\_str\_\_ as a fall back

3. \_\_bool\_\_:
   * If \_\_bool\_\_ is not implemented, Python will invoke \_\_len_\_\_, and return False if that returns zero

4. \_\_len_\_\_ will read from a field in a C struct makes it more quicker than using a len(Object) method when using built-in objects.