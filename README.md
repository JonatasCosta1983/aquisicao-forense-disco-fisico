# Aquisição física feita com duas ferramentas diferentes para determinar se a montagem do disco foi feita automaticamente e se os hash são iguais. 

Laboratório para comparar uma aquisição física feita com o EnCase Acquisition e o Guymager. 

Para esse teste foi usado um notebook Dell Vostro 3500 i7 8gb SSD 256 com placa de vídeo iris com dual boot Windows 10 e Ubuntu 4:5.18.7-0ubuntu0.1.  

Em toda aquisição forense cuidados com a montagem automática do disco e bloqueio de escrita são necessários para que as possíveis provas ali recuperadas tenham validade nos tribunais. 

Nesse teste foi usado um HD 160GB como dispositivo questionado e um adaptador sata USB 3.0 com fonte.

Agora no sistema Ubuntu antes de conectar o disco, a montagem automática está desabilitada. Caso você não saiba desabilitar a montagem no Ubuntu, segue o link de um artigo que eu explico como desabilitar a montagem automática de disco no Linux;  https://www.linkedin.com/pulse/uma-abordagem-gr%C3%A1fica-sobre-como-desabilitar-montagem-jonatas-costa/ 

 
Com o disco conectado o comando sudo fdisk - l lista todos os discos conectados que estão em /dev. 

Digitando o comando: cd  /media  

Esse comando lista todos os discos montados no sistema. 

 Na imagem acima fica claro que nem um disco foi montado. 

Agora com o Guymager aberto a aquisição física será executada.  

Após a aquisição pelo Guymager, podemos ver que o hash é df917a811126ff7ace4283bc8f57e197. 

Agora com o sistema Windows 10 o disco questionado será inserido, mas antes com o uso da ferramenta EnCase Acquisition será ativado o bloqueio de escrita. 

Como é possível observar o bloqueio de escrita é ineficaz com o uso de adaptador do tipo sata 3.0 com disco conectado a ele. 

Para melhor compreensão, o disco será conectado novamente ao sistema Ubuntu que tem a montagem automática de discos desabilitada e o cálculo de hash será calculado novamente. 

Com o comando md5sum /endereço do disco o hash foi recalculado.  

Como foi possível determinar o hash do disco foi modificado devido a ferramenta EnCase Acquisition não bloquear a escrita do dico via adaptador usb sata 3.0. 

Como segundo experimento, o mesmo teste será corrido com um pen-drive de 4GB. 

MD5 hash com FTK imager :    2b928fbed619e4d7cf106cd320907ea0 

MD5 hash com Guymager   :    2b928fbed619e4d7cf106cd320907ea0 

Então é possível determinar que no uso de um pen-drive o disco não foi modificado em ambas as ferramentas. 