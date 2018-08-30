# Sistema de monitoramento com alarme para MSP430
Sistema simples de monitoramento com alarme, desenvolvido em Assembly, para a plataforma MSP430. Testado com os MCUs MSP430G2553 e MSP430G2452.

***
* Descrição:<br>
  - O sistema conta com um sensor de presença, buzzer, teclado 4x4 e display 16x2.
  - Possui uma senha de 8 dígitos para sua validação, esta senha pode ser alterada a desejo do usuário e será salva na FLASH do MCU (Endereço definido no código).
  - Ao resetar o sistema com a tecla # pressionada, a senha default (00000000) é definida.
  - Quando o usuário digitar a senha incorretamente por 5 vezes, o sistema será travado e só será liberado após o reset.
  - Ao digitar o oitavo dígito o sistema irá validar qualquer senha digitada, porém quando estiver digitando, o usuário poderá pressionar o "#" para limpar o display e começar novamente. 
  - É possível ativar ou desativar o monitoramento do sensor; ao desativar, o sistema entrará em standby, desativando o display e o MCU; ao ativar, o sistema contará 30 segundos para a ativação e após o tempo entrará em modo de standby, porém será despertado com a ativação do sensor.
  - Quando o sensor for ativado e o monitoramento estiver ligado o buzzer será acionado;
  - Ao validar a senha o buzzer será desativado e o monitoramento idem;
  - Quando o sistema entrar em standby o pressionamento de qualquer tecla o despertará e só voltará a entrar nesse modo quando o usuário ativar ou desativar o monitoramento.
 
 ***
 * Conexões:
 <div align="center"><img width="600px" src="https://imgur.com/download/7TvHIdD"/></div>

***
* Observações:
  - Sensor utilizado: HC-SR501
  - Utilize buzzer ativo; para buzzer passivo será necessário implementar um oscilador a parte.  
 
