# Sistemas operativos - xv6 (practica 2)
![Proceso](imgs/proces.png)

---
Esta imagen es un resumen de todo lo que se hace cuando haces una syscall al kernel que en este caso es xv6.
En resumen es importante usar un trapframe , para que al momento de terminar el ecall la aplicaciòn siga funcionando con normalidad ya que el *trapframe* es importante por que ahi se guarda los estados de xv6 cuando ocurre un trap. 

Entre los registros que se guardan se encuentra a7 que este conntiene el numero de la llamada al sistema pero antes *usetrap* usa otra funciòn muy importante llamada **rscause()=8** 8 es para decir que ocurrio un llamado  al sistema.Entonces como esta en el grafico se ejecuta *syscall()* que obtiene desde p->frame->a7 el nùmero de syscal l para determinar que funcion se ejecuta.

