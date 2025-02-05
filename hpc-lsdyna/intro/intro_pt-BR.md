# Introdução

A Computação de Alto Desempenho está mudando o desenvolvimento e a pesquisa de produtos, permitindo que os clientes resolvam problemas complexos mais rapidamente. Isso significa menos protótipos, acelera os testes e diminui o tempo de entrada no mercado. A Oracle oferece infraestrutura HPC sob demanda, adequada a qualquer carga de trabalho HPC, com base nas mais avançadas tecnologias de computação, armazenamento, rede e software. Você obtém tudo isso a uma fração do custo de desenvolvê-lo sozinho e evita problemas de utilização de capacidade.

A Oracle fornece a infraestrutura de nuvem mais elástica e escalável para executar seus aplicativos HPC. Com capacidade virtualmente ilimitada, engenheiros, pesquisadores e proprietários de sistemas HPC podem inovar além das limitações da infraestrutura HPC local. A Oracle oferece um conjunto integrado de serviços que fornece tudo o que é necessário para criar e gerenciar de forma rápida e fácil clusters HPC na nuvem para executar as cargas de trabalho mais intensivas em computação em vários setores verticais. Essas cargas de trabalho abrangem os aplicativos HPC tradicionais, como genômica, química computacional, modelagem de risco financeiro, engenharia auxiliada por computador, imagens sísmicas e previsão do tempo, bem como aplicativos emergentes, como aprendizado de máquina, aprendizado profundo e condução autônoma.

Com o Oracle Cloud Infrastructure, as empresas podem executar cargas de trabalho de HPC que requerem milhões de IOPs, milissegundos de latência e muitos GB/s de largura de banda, em um modelo de pagamento por uso ou não, economizando 32% em um TCO de 3 anos.

Esses guias práticos de laboratório oferecem o processo passo a passo de implantar um cluster LS Dyna no Oracle Cloud com rede de baixa latência entre os nós de computação. Executar o LS Dyna no Oracle Cloud é bem óbvio, siga este guia para todas as dicas e truques.

Tempo Estimado do Workshop: 100 minutos

## Sobre a Computação de Alto Desempenho (HPC)

HPC, ou supercomputação, é como computação diária, apenas mais poderosa. É uma maneira de processar grandes volumes de dados em velocidades muito altas usando vários computadores e dispositivos de armazenamento como um tecido coeso. A HPC permite explorar e encontrar respostas para alguns dos maiores problemas do mundo em ciência, engenharia e negócios.

Uma rede de clusters é um pool de instâncias de computação de alto desempenho (HPC) conectadas a uma rede de alta largura de banda e latência ultrabaixa. Cada nó do cluster é uma máquina bare metal localizada próxima aos outros nós. Uma rede RDMA (remote direct memory access) entre nós fornece latência tão baixa quanto microssegundos com um único dígito, comparável aos clusters HPC locais.

A Computação de Alto Desempenho é oferecida no Oracle Cloud Infrastructure, nas regiões da OCI.

Instância de Computação de Alto Desempenho disponível no Oracle Marketplace Image e BM.HPC2.36 no OCI.

O rack de Computação de Alto Desempenho na Imagem do Oracle Marketplace inclui nós de cluster HPC, rede de clusters e compartilhamento NFS.

Os nós de computação são conectados por meio da rede de clusters, que oferece acesso de armazenamento baseado em RDMA aos nós de computação.

Atualmente, há suporte para um único BM por nó de computação. Ele permite o acesso raiz para os clientes durante a proteção de hardware e rede, os nós de computação são virtualizados usando o BM.HPC2.36.

### Objetivos

Neste laboratório, você:

*   Ativar Rede de Clusters HPC
*   Acesse seu cluster
*   Configurar Visualização
*   Acessar sua VNC
*   Instalar LS-DYNA
*   Executar LS-DYNA

### Pré-requisitos

*   Algum entendimento dos termos de nuvem e banco de dados é útil
*   Familiaridade com o OCI (Oracle Cloud Infrastructure) é útil
*   A familiaridade com a rede é útil

## Sobre este Workshop

*   Inicie uma Rede de Clusters de Computação de Alto Desempenho no Oracle Cloud Infrastructure
*   Acessar seu cluster usando o endereço IP público do bastion
*   Crie e configure Ferramentas de Visualização para sua simulação usando o nó de Visualização GPU
*   Acessar sua VNC conectando-se por meio de um túnel SSH
*   Instale o LS-DYNA em sua instância adicionando todas as bibliotecas e arquivos binários necessários
*   Executar LS-DYNA

## Confirmação

*   **Autor** - Equipe de Computação de Alto Desempenho
*   **Contribuidores** - Chris Iwicki, Harrison Dvoor, Gloria Lee, Selene Song, Bre Mendonca, Samrat Khosla
*   **Data da Última Atualização** - Samrat Khosla, Outubro de 2020

# <<<<<<<<< CABEÇALHO

> > > > > > > upstream/mestre