# Ejercicios de DIP, ISP, SRP
## Ejercicio 1 

**DIP:** No se cumple porque la clase de mayor, AnalizadorDatos, depende de detalles de la clase de menos nivel, BasedeDatos. El caso se da en el public void Analizar donde la clase AnalizadorDatos debe saber el bool que le devuele la función Cumplecondicion() que recibe un objeto DataBaseObject.

**ISP:** se cumple o no y por que

**SRP:** La clases DataBaseObject, AnalizadorDatos cumplen con el SRP porque tienen solo una razón de cambio. Pero la clase AnalizadorDatos a parte de analizar los objetos DataBaseObject, también tiene que verificar que dichos objetos cumplan una condición.


## Ejercicio 2

```cs
//Insertar el código corregido
class DataBaseObject : IDataBaseObject
{
    public string Descripcion { get; }
    public bool Condicion();
}

//Base de datos.
class BaseDeDatos
{
    public DataBaseObject ObtenerDato(string clave)
    {
        //Devuelve el dato correspondiente a la clave
    }
    public void GrabarDato(string clave, DataBaseObject dato)
    {
        //Graba el dato en la base de datos, bajo la clave dada
    }
    public String[] ListarClaves()
    {
        //Devuelve un String[] con todas las claves
    }
    public String[] ListarDescripcionDatos()
    {
        //Devuelve un String[] con la descripción de todas los 
        //datos almacenados en  la base
    }
    public DataBaseObject[] ListarDatos()
    {
//Devuelve un DataBaseObject[] con todos los datos almacenados en la base
    }
}
public interface IDataBaseObject
{
    string Descripcion();
    bool Condicion();
}
class AnlizadorDatos
{
    private BaseDeDatos baseDatos{get; set;};
    public void Analizar()
    {
        foreach (DataBaseObject DBObj in baseDatos.ListarDatos())
        {
            if (DBObj.Condicion())
            {
                MensajeUno();
            }
            else
            {
                MensajeDos();
            }
        }
    }
    public void MensajeUno()
    { /*Mensaje predeterminado*/ }
    public void MensajeDos()
    { /*Mensaje predeterminado*/ }
}

```
## Ejercicio 3 

```cs
////Insertar el código corregido. El ejercicio 2 y 3 pueden ser resueltos de forma conjunta

```