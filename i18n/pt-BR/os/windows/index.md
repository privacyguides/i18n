---
title: Visão geral do Windows
icon: material/microsoft-windows
description: O Microsoft Windows é o sistema operacional comum utilizado pela maioria dos desktops e é considerado extremamente <0>nocivo</0> à privacidade em sua configuração original. Nosso guia cobre informações relacionadas a procedimentos que melhoram a privacidade de seu computador sem a necessidade de trocar seu sistema operacional.
---

**Microsoft Windows** é um sistema operacional instalado por padrão na maioria dos PCs (computadores de uso pessoal) Os guias seguintes visam prover informações e meios para melhorar a privacidade e reduzir a telemetria e dados pessoais através da desativação de recursos desnecessários e/ou invasivos. Com o passar do tempo, a Microsoft adicionou recursos em seu sistema operacional que podem em determinadas situações depender de serviços 'na nuvem'. Esses recursos dependem de [dados opcionais](https://www.microsoft.com/pt-br/privacy/data-collection-windows) enviados para servidores remotos de modo a serem processados

Um dos exemplos mais recentes foi chamado de **Recall**, uma parte do conjunto de recursos de IA do Copilot. Recall periodicamente faz **capturas de tela** de tudo o que você viu no PC para mostrá-lo posteriormente. Esses recursos "úteis" criam metadados consideráveis que podem ser analisados forensicamente. Na maioria dos casos, o histórico de navegação é suficiente e esse recurso pode ser desativado com segurança. A principal preocupação com o Recall é que os dados são armazenados em um banco de dados local que é descriptografado quando o dispositivo é ligado, o que significa que é um alvo fácil para os hackers se o dispositivo for infectado por malware (programa ou código malicioso). O Recall não eliminará informações confidenciais, como senhas copiadas ou informações financeiras do banco de dados, mas protege contra a realização de capturas de tela de qualquer conteúdo protegido por direitos autorais e protegido por sistemas de gerenciamento de direitos digitais (DRM).

Infelizmente, esse recurso foi adicionado sem muita reflexão sobre as implicações de privacidade de ter esse recurso ativado por padrão (o que mudou [atualmente](https://wired.com/story/microsoft-recall-off-default-security-concerns)). Esse não é um exemplo isolado outro exemplo, da mesma companhia, foi a [ativação automática](https://neowin.net/news/windows-11-is-now-automatically-enabling-onedrive-folder-backup-without-asking-permission) de backups de pastas no OneDrive  em novas instalações do Windows 11 sem pedir permissão de seus usuários.

Com estes guias você pode melhorar a privacidade e segurança no Windows sem baixar nenhuma ferramenta de terceiros:

- Instalação Inicial
- [Configurações de Políticas de Grupos](group-policies.md)
- Configurações de privacidade (em breve)
- Sandboxing de aplicativos (em breve)
- Melhorias na Segurança (em breve)

<div class="admonition example" markdown>
<p class="admonition-title">Esta seção é **nova**</p>

_Esta seção é um trabalho em andamento, pois é preciso muito mais tempo e esforço para tornar uma instalação do Windows mais favorável à privacidade do que outros sistemas operacionais._

</div>

## Nota de Privacidade

O Microsoft Windows, especialmente as versões voltadas para os consumidores, como a versão **Home**, geralmente não prioriza recursos favoráveis à privacidade por [padrão](https://theguardian.com/technology/2015/jul/31/windows-10-microsoft-faces-criticism-over-privacy-default-settings). Como resultado, podemos observar a [coleta de dados](https://en.wikipedia.org/wiki/Criticism_of_Microsoft#Telemetry_and_data_collection) numa intensidade bem maior do que se julgaria necessário, sem conter nenhum aviso de que esse é o comportamento padrão do sistema. Numa tentativa de competir com o Google no âmbito publicitário, a [Cortana](https://pt.wikipedia.org/wiki/Cortana_\(virtual_assistant\)) incluiu identificadores exclusivos, como um "ID de publicidade", para correlacionar o uso e auxiliar empresas anunciantes na publicidade direcionada.  No lançamento do Windows 10 não era possivel desativar a telemetria em licenças não corporativas do sistema operacional. Ainda não é possível desativar por completo mas a Microsoft adicionou recursos para [reduzir](https://extremetech.com/computing/243079-upcoming-windows-update-reduces-spying-microsoft-still-mum-data-collects) a quantidade de dados enviados.

No Windows 11 há uma série de restrições ou padrões pré-definidos como:

- Exigir a autenticação ode uma conta da Microsoft em vez de uma conta local.
- Tornando cada vez mais difícil encontrar opções de contas locais para o Windows em suas versões **Pro** e **Enterprise**.
- Manter ativadas todas as opções de coleta de dados por padrão, forçando seus usuários a desabilitar manualmente.
- Promovendo a integração forçada de outros serviços da companhia como o Edge, Bing, OneDrive e o Teams ao sistema Windows, de forma que dificulta a remoção dos mesmos, tornando-os as únicas opções para usuários inexperientes.
- Mantendo o Microsoft Edge como navegador padrão, eventualmente revertendo para o mesmo caso modificado.
- Adicionando recursos baseados 'em nuvem' e agentes de IA em várias áreas do sistema Windows e outros aplicativos da Microsoft.
- Armazenamento desnecessário de dados confidenciais. Mesmo que os dados estejam localmente armazenados e não sejam enviados para a Microsoft eles ainda podem ser um alvo para hackers, malwares e ameaças de todo tipo.

A Microsoft geralmente utiliza seu recurso de atualizações automáticas para adicionar novos recursos e funcionalidades que podem coletar dados, configurações que são ativadas por padrão. Alguns [recursos de privacidade](https://blogs.windows.com/windows-insider/2023/11/16/previewing-changes-in-windows-to-comply-with-the-digital-markets-act-in-the-european-economic-area), como a opção de _optar por sair_ da sincronização de uma conta Microsoft on-line com o Windows, exigem que você selecione um país no EEE (Espaço Econômico Europeu) durante a instalação. Você pode alterar para o seu país original depois que a instalação for feita.

## Edições do Windows

Infelizmente, muitos recursos essenciais de privacidade e segurança estão bloqueados nas edições de custo mais baixo do Windows, em vez de estarem disponíveis no Windows **Home**. Alguns recursos ausentes na edição **Home** do Windows incluem o BitLocker Drive Encryption, Hyper-V e Windows Sandbox. Em nossos guias voltados para o Microsoft Windows, abordaremos como usar todos esses recursos adequadamente, portanto, será necessário ter uma edição 'premium' (Pro, Educational ou Enterprise' do Windows.

O Windows **Enterprise** oferece a maior flexibilidade quando se trata de configurar as definições de privacidade e segurança incorporadas ao Windows. São as únicas edições que permitem que você ative o mais alto nível de restrições nos dados enviados à Microsoft por meio de ferramentas de telemetria. Infelizmente, o Windows em sua versão Enterprise não está disponível para compra no varejo, portanto, pode não estar disponível para você.

A melhor versão disponível para compra no varejo é o Windows **Pro**, pois possui quase todos os recursos que você deseja usar para proteger seu dispositivo, incluindo BitLocker, Hyper-V, etc. A única coisa que falta são algumas das limitações mais restritivas da telemetria da Microsoft, infelizmente.

Os alunos e professores podem obter uma licença do Windows **Education** (equivalente a Enterprise) ou **Pro Education** (equivalente a Pro) gratuitamente, inclusive em dispositivos pessoais, de sua instituição de ensino. Muitas escolas e universidades fazem parceria com a Microsoft por meio do OnTheHub ou do Microsoft Azure for Education, portanto, você pode conferir se esses benefícios são aplicáveis a instituição que você estuda. O fato de você conseguir ou não obter essas licenças depende inteiramente de sua instituição. Para muitos, essa pode ser a melhor maneira de obter uma edição de nível empresarial do Windows para uso pessoal. Não há riscos adicionais à privacidade ou segurança associados ao uso de uma licença educacional em comparação com as versões de varejo.

Não é recomendável usar versões modificadas do Windows de terceiros, como o Windows AME. Como essas versões não-oficiais de Windows como o AME não recebem atualizações correntes do sistema e recursos de segurança como definições e filtros do Windows Defender. Essas distribuições customizadas do Windows podem ficar defasadas em relação ao cenário atual de ameaças digitais, tornando sua máquina desprotegida de ataques e invasões.

## Adquirindo o Windows

Atualmente, apenas licenças do Windows 11 estão disponíveis para compra, mas essas chaves (serial key) também funcionarão no Windows 10, portanto, ainda é possível comprar uma chave do Windows 11 Pro para ativar uma instalação do Windows 10.

A ferramenta [Criação de Mídia] oficial (https://microsoft.com/software-download/windows11) é a melhor maneira de gravar um instalador do Windows em um pendrive ou cartão de memória. Ferramentas de terceiros, como o Rufus ou o Etcher, podem modificar alguns arquivos, gerando problemas de inicialização ou durante a instalação.

Essa ferramenta só permite que você instale uma instalação **Home** ou **Pro**, pois não há downloads disponíveis publicamente para a edição **Enterprise** do Windows. Se você tiver uma chave de licença **Enterprise**, poderá facilmente migrar para a versão **Pro**. Para fazer isso, instale o Windows **Pro** sem inserir uma chave de licença durante a configuração e, em seguida, insira sua chave **Enterprise** no aplicativo Configurações após concluir a instalação. Sua instalação **Pro** será atualizada para **Enterprise** automaticamente após a inserção de uma chave de licença válida.

Se estiver instalando uma licença **Educação**, você normalmente receberá um link privado para download que contará com a chave de licença educaional. Geralmente o portal de benefícios da sua instituição é quem provê a chave e o link.
