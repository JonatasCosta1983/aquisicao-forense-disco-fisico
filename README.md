# Aquisição física com duas ferramentas diferentes para determinar se a montagem do disco não foi feita automaticamente e se os hash são iguais. 

Laboratório para comprar uma aquisição física feita com o FTK imager e o Guymager. 

Em toda aquisição forense cuidados com a montagem automática do disco e bloqueio de escrita são necessários para que as possíveis provas ali recuperadas tenham validade nos tribunais. 

Nesse teste foi usado um HD 160GB como dispositivo questionado e um adaptador sata USB 3.0 com fonte. 

Agora no sistema Ubuntu antes de conectar o disco, a montagem automática está desabilitada. Caso você não saiba desabilitar a montagem no Ubuntu, segue o link de um artigo que eu explico como desabilitar a montagem automática de disco no Linux;  https://www.linkedin.com/pulse/uma-abordagem-gr%C3%A1fica-sobre-como-desabilitar-montagem-jonatas-costa/ 

Com o disco conectado: em /dev
Digitando o comando: cd  /media  
Esse comando lista todos os discos montados no sistema. 

Agora com o Guymager aberto a aquisição física será executada.  

