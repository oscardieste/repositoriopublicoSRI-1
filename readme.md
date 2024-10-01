# Repositorio Público SRI 1

## Preguntas

1. **Descargar e comprobar que unha imaxe está no teu equipo**
   Para descargar a imaxe de Ubuntu, utilizamos o comando `docker pull ubuntu`. Para verificar que a imaxe se descargou correctamente, utilizamos `docker images`, que mostrará unha lista de todas as imaxes dispoñibles no teu equipo.

2. **Crear un contenedor sen nome, queda arrincado?, cómo obtés o nome?**
   Podemos crear un contenedor sen nome executando `docker run -d ubuntu`. O contenedor seguirá en execución en segundo plano, e podemos obter o seu ID usando `docker ps -a`, que mostrará todos os contenedores, incluídos os que non teñen nome.

3. **Crea un contenedor co nome 'u1', cómo accedes a el?**
   Para crear un contenedor nomeado 'u1', utilizamos `docker run -d --name u1 ubuntu`. Para acceder á consola do contenedor, utilizamos `docker exec -it u1 bash`, que nos permitirá interactuar co sistema operativo do contenedor.

4. **Comproba a súa IP e fai ping a google.com**
   Podemos comprobar a IP do contenedor 'u1' executando `docker inspect u1 | grep "IPAddress"`. Despois, accedemos ao contenedor e realizamos un ping a google.com para verificar a conectividade.

5. **Crea un contenedor co nome 'bono', pódes facer ping entre os contenedores?**
   Para crear un segundo contenedor nomeado 'bono', utilizamos `docker run -d --name bono ubuntu`. Para comprobar a conectividade entre os contenedores, podemos realizar un ping desde un contenedor ao outro unha vez que ambos estén en execución.

6. **Se pechas as terminales, qué pasa co contenedor?**
   Se o contenedor foi creado co parámetro `-d`, continuará en execución en segundo plano, incluso se pechas a terminal. Se non se usou `-d`, o contenedor parará ao pechar a terminal.

7. **Cánta memoria no disco duro ocupaches? usa docker para calculalo**
   Para comprobar o espazo en disco ocupado por imaxes e contedores, utilizamos `docker system df`. Este comando proporciona un resumo do uso do disco en relación coas imaxes, contedores e volumes de Docker.

8. **Cánta RAM ocupan os contenedores? Crea varios para calculalo**
   Podemos utilizar `docker stats` para ver o uso en tempo real da RAM dos contenedores en execución. Para crear varios contenedores, simplemente repetimos o comando `docker run -d --name <nome> ubuntu` para cada un deles.

9. **Cómo fixeches para clonar o repositorio?**
   Para clonar o repositorio que creaches en GitHub, usamos o comando `git clone <URL_del_repositorio>`, que copia todo o contido do repositorio remoto á túa máquina local.

10. **Cómo engades o arquivo readme2.md?**
    Para engadir o arquivo readme2.md, primeiro creámolo co comando `echo "frase que poñamos a elección" > readme2.md`, despois engadímolo á área de preparación de Git con `git add readme2.md`.

11. **Os pasos a seguir para subir o arquivo que estás editando e o arquivo readme2.md**
    Para subir os cambios, primeiro realizamos un commit co comando `git commit -m "Mensaxe do commit"`, e despois subimos os cambios ao repositorio remoto con `git push origin main`.

12. **Cómo comprobarías que existen diferencias entre o teu repositorio local e o remoto?**
    Para comprobar as diferenzas entre o repositorio local e o remoto, utilizamos `git fetch` para obter os cambios do remoto e `git diff origin/main` para ver as diferenzas entre a rama local e a remota.


