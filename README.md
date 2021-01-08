# BaseLibrary
## Base库

### 包含了：

~ MVP的BaseInterface和BaseImplement

~ RxView依赖

~ dagger依赖

~ RxUtil，方便线程切换


#### RxUtil.kt

 object RxUtil {
    fun <T> ioToMainTransformer(): ObservableTransformer<T, T>

    fun <T> mainToIoTransformer(): ObservableTransformer<T, T> 
    
    fun <T> mainToComputationTransformer(): ObservableTransformer<T, T> 

    fun <T> computationToMainTransformer(): ObservableTransformer<T, T>
    
    fun <T> autoDisposeOnComplete(observable: Observable<T>,onNext: Consumer<T>)
   }
