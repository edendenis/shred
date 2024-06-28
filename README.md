# Como configurar/instalar/usar o `shred` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para configurar/instalar/usar o `shre` no `Linux Ubuntu`.

## _Abstract_

_This document contains the main commands and configurations to configure/install/use the `shred` on `Linux Ubuntu`._

## Descrição [2]

### `shred`

O comando `shred` é uma ferramenta de linha de comando encontrada em sistemas Unix-like, incluindo `Linux`, que é projetada para a remoção segura de arquivos e dados em discos rígidos e outros dispositivos de armazenamento. O `shred` substitui o conteúdo dos arquivos com dados aleatórios, tornando muito difícil ou praticamente impossível a recuperação dos dados originais. Essa técnica é especialmente útil quando se deseja garantir que informações confidenciais não possam ser recuperadas por meio de métodos de recuperação de dados convencionais. O `shred` permite que os usuários definam o número de vezes que os dados são sobrescritos e pode ser usado com uma variedade de opções para personalizar o processo de destruição segura de dados, tornando-o uma ferramenta valiosa para a proteção da privacidade e segurança de dados sensíveis.

## 1. Como configurar/instalar o `shred`no `Linux Ubuntu` [1][3]

Para configurar/instalar o `shred` no `Linux Ubuntu`, você pode seguir estes passos:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`    

2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.2 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`: `sudo apt update`

    2.5 **Corrigir pacotes quebrados**: Isso atualizará a lista de pacotes disponíveis e tentará corrigir pacotes quebrados ou com dependências ausentes: `sudo apt --fix-broken install`

    2.6 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.7 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:  `sudo apt list --upgradable`

    2.8 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update`. Digite o seguinte comando e pressione `Enter`: `sudo apt full-upgrade -y`
    

O `HDShredder` é uma ferramenta especializada para apagar dados de dispositivos de armazenamento de forma segura. No entanto, até a última atualização do meu treinamento em abril de 2023, o `HDShredder` estava disponível apenas para sistemas operacionais Windows. Não havia uma versão oficial para Linux.

Para usuários de Linux que desejam apagar dados de forma segura, existem alternativas ao `HDShredder`. Uma das ferramentas mais populares para esta finalidade no Linux é o `shred`, que já vem pré-instalado em muitas distribuições. Aqui está um guia básico de como usar o `shred`:

3. **Identifique o Dispositivo de Armazenamento:** Antes de apagar qualquer coisa, você precisa identificar o dispositivo de armazenamento que deseja apagar. Você pode listar todos os dispositivos de armazenamento e suas partições com o comando `lsblk`.

4. **Use o Comando Shred:** O comando básico para usar o `shred` é: `sudo shred -vzn 0 /dev/sdX`

    Onde `/dev/sdX` é o caminho para o dispositivo que você quer apagar (`sdX` deve ser substituído pelo identificador correto do seu dispositivo, como `sda` ou `sdb`). O parâmetro -`v` ativa o modo verboso, -`z` adiciona uma passagem final de zeros para ocultar o shredding, e `-n 0` especifica o número de passagens (altere conforme necessário).

**Atenção:** Este processo é destrutivo e irrecuperável. Certifique-se de que está apagando o dispositivo correto e de que você não precisa dos dados nele contidos.

Se você ainda preferir usar o `HDShredder` no Linux, uma opção seria usar uma máquina virtual com Windows ou criar um boot dual para poder executá-lo em um ambiente Windows.

### 1.1 Código completo para configurar/instalar

Para configurar/instalar/usar para limpar o histórico dos navegadores no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Digite o seguinte comando e pressione `Enter`:

    ```
    NÂO há.
    ```


## Referências

[1] OPENAI. ***Instalando o hdshredder no linux.*** Disponível em: <https://chat.openai.com/c/0c8f694b-1d08-475a-bb81-bb4e5d3369ac> (texto adaptado). ChatGPT. Acessado em: 28/01/2024 23:03.

[2] OPENAI. ***Vs code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). ChatGPT. Acessado em: 28/01/2024 23:03.

