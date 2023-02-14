# Servidor duck & Robots
## _Informe de mi primer laboratorio_


En mi primer laboratoro, el cliente solicito migrar su sitio web a AWS   ya que estaba teniendo alta demanda y en multiples ocasiones se le cayo el sitio web debido a que el servidor no soportaba tanto trafico .

Se diseño un networking(VPC) con  dos  subredes publicas , dos   subredes privadas con acceso a internet a traves de NAT y dos subredes privadas para databases sin acceso a internet
Para acceder a los servidores se hizo a traves de un Bastion Host para mas seguridad con acceso a traves de SSH por medio del puerto 22 

Se decidio usar nginx  como servidor web de los servidores creados para la pagina de duck y robots, en donde duck cuenta con dos servidores adicionales en subredes privadas 

Como la demanda cada vez crece mas en los servidores de duck y robots se balanceo el trafico a travez de un ALB     el cual se creo en una subred publica redireccionando cada uno por un puerto diferente 

