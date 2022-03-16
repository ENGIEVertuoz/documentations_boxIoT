# Plugin Velux MQTT

O plug-in **Velux MQTT** irá permitir-lhe controlar as suas clarabóias em Jeedom através da interface VELUX KLF 200 e controlar a sua posição, subindo ou descendo e parando.

As clarabóias devem primeiro ser emparelhadas com a interface VELUX KLF 200 e devem ser conectadas em ethernet na mesma rede local que Jeedom *([veja a documentação do KLF 200](https://www.domadoo.fr/fr/index.php?controller=attachment&id_attachment=2287){:target="\_blank"})*.

# Configuration

Como qualquer plugin Jeedom, o plugin **Velux MQTT** deve ser ativado após a instalação.

## Gerenciamento de dependência

O plug-in **Velux MQTT** depende de plugins oficiais **Gerenciamento do Docker** e **Gerente MQTT** trabalhar. Se ainda não foi o caso, esses 2 plugins serão instalados durante a instalação das dependências.

>**EM FORMAÇÃO**
>
>A instalação de dependências provavelmente levará vários minutos dependendo das configurações.

## Gerente MQTT

Um broker MQTT deve estar configurado e ativo no plugin **Gerente MQTT** para transmitir e recuperar as posições das clarabóias. Consulte a documentação do plugin para usar um corretor existente ou para criar um localmente no Jeedom.

Assim que o plugin daemon **Gerente MQTT** estará ativo, o plugin **Velux MQTT** poderá recuperar automaticamente as informações de conexão do agente MQTT.

## Configuração do plug-in

A configuração do plugin consiste em preencher as informações de conexão para a interface VELUX KLF 200 :

- **Endereço de IP** : O endereço IP do KLF200 na rede local.
- **Senha do wifi** : A senha WiFi KLF200 *(inscrito nas costas)*.

## Instalando o contêiner Velux MQTT

Uma vez que as informações de conexão para a interface VELUX KLF 200 tenham sido inseridas e salvas, clique no botão **Instale o VELUX MQTT** para verificar se está tudo em ordem e prosseguir com a criação do container **Velux MQTT** em plug-in **Gerenciamento do Docker**.

No final do procedimento, os estatutos do estivador **Velux MQTT** deve ser exibido em verde com as palavras *"running"* e *"CONNECTED"*. Caso contrário, verifique os logs do dispositivo **Velux MQTT** em plug-in **Gerenciamento do Docker**.

# Equipements

Para aceder aos vários equipamentos Velux, aceda ao menu **Plugins → Protocolo de automação residencial → Velux MQTT**.

O botão **Para sincronizar** permite criar automaticamente o equipamento correspondente às clarabóias listadas na interface KLF 200 no Jeedom.

# Commandes

Cada equipamento **Velux MQTT** tem esses comandos :

- **Estado** : posição atual da clarabóia.

>**TRUQUE**
>
>Por padrão, a interface KLF 200 fornece uma porcentagem de fechamento *(100% = fechado)* que o plugin transforma em porcentagem aberta. Se você quiser retornar à operação padrão, basta desmarcar a caixa **Reverter** da ordem **Estado**.

- **Posição** : Controle de posicionamento da clarabóia.
- **Abrir** : Comando de abertura da clarabóia.
- **Pare** : Comando de parada da clarabóia.
- **Fechar** : Comando de fechamento da claraboia.