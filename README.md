# Ev_2.1
class Estudiante:
    def __init__(self, nombre, edad, calificacion):
        self.nombre = nombre
        self.edad = edad
        self.__calificacion = calificacion 
    @property
    def calificacion(self):
        return self.__calificacion


    def mostrar_informacion(self):
        print(f"Nombre: {self.nombre}")
        print(f"Edad: {self.edad} años")
        print(f"Calificación: {self.calificacion}")

   
    def actualizar_calificacion(self, nueva_calificacion):
        if 0 <= nueva_calificacion <= 100:
            self.__calificacion = nueva_calificacion
            print("Calificación actualizada con éxito.")
        else:
            print("La calificación debe estar en el rango de 0 a 100.")


estudiante1 = Estudiante(nombre="Juan", edad=20, calificacion=85)


print("Información del Estudiante:")
estudiante1.mostrar_informacion()


print(f"Calificación del estudiante: {estudiante1.calificacion}")


estudiante1.actualizar_calificacion(90)


print("\nInformación actualizada del Estudiante:")
estudiante1.mostrar_informacion()
