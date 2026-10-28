# Widget do Escobar - WE

Widget de recursos do sistema (CPU, GPU, RAM e rede) para Windows. Baixe em **Code → Download ZIP**, extraia a pasta inteira e abra `PainelSistema.exe` ou `Iniciar Widget.bat`. Não exige Python instalado. Windows 64 bits. (O arquivo mantém o nome `PainelSistema.exe` para que versões anteriores reconheçam a atualização.)

Versão: **1.2.0**.

Arraste para mover (a posição é salva ao soltar, inclusive em monitores secundários). Dê dois cliques para abrir **Configurações**. A janela de configurações também pode ser arrastada: clique e arraste em qualquer área vazia, principalmente no cabeçalho; ela reabre onde você a deixou. As opções destacam-se ao passar o mouse, e Esc ou o X do cabeçalho fecham o menu.

- Visão: Tudo, Só gráficos ou Só círculos.
- Orientação: Deitado ou Empilhado (vertical).
- Escala: de 50% a 150%. Em telas baixas, use escala menor ou a visão circular para empilhar quatro indicadores.
- Métricas: CPU, GPU, RAM e rede; pelo menos uma permanece ativa.
- GPU: placas NVIDIA, AMD (Radeon) e integradas (Intel UHD/Iris/Arc e AMD Radeon Graphics). Uso e memória vêm dos mesmos contadores do Gerenciador de Tarefas; em placas integradas a memória mostrada é a compartilhada. Em **Placa de vídeo**, clique para alternar entre Automática (prefere a dedicada) e cada placa detectada.
- Sensores: **Temperatura da CPU** e **Temperatura da GPU** podem ser ligadas ou desligadas. A GPU usa a temperatura informada pelo driver (ou nvidia-smi em NVIDIA). Para a CPU, o Windows não oferece leitura precisa sem um driver: deixe o [LibreHardwareMonitor](https://github.com/LibreHardwareMonitor/LibreHardwareMonitor) aberto e o widget passa a ler CPU e GPU por ele; sem ele, usa a zona térmica ACPI quando existir (aproximada) ou mostra traço. O menu informa a fonte usada. Com as temperaturas ligadas, um PowerShell oculto e de baixa prioridade fica aberto para consultar o LibreHardwareMonitor; ele encerra junto com o widget.
- Temas: Original, Grunge, Nexus (HUD), Ironworks (analógico), Mono, Phosphor (terminal), Mixer (console), Orbit (planetas), Glass (vidro), Blueprint (esquemático), Stack (cartões) e Spectrum (barras dinâmicas).
- Em Configurações, clique em **Temas** para abrir a janela de miniaturas. Clique em qualquer bloco para aplicar o visual imediatamente. A janela continua aberta para experimentar outras opções; use a rolagem para ver todos e **Fechar**, X ou Esc quando terminar. A escolha fica salva. O seletor pode ser movido e redimensionado e não bloqueia o widget.
- Sempre visível: mantém o widget sobre as janelas comuns. Jogos em tela cheia exclusiva e a área de trabalho segura do Windows podem se sobrepor.
- Atualizar widget: consulta o repositório público no GitHub ao clicar. Mostra a versão instalada e avisa se há uma versão mais nova. O botão de download abre o ZIP do GitHub no navegador; extraia em uma pasta de sua escolha. Para substituir a instalação, feche o widget antes e preserve `painel_sistema.cfg`. Não substitui arquivos automaticamente nem exige Git instalado.
- Inicializar com Windows: ativa/desativa a abertura ao entrar na sua conta, sem privilégios de administrador. Só é ativada por você. Se mover a pasta, desmarque e marque novamente. Desmarque antes de remover o programa.

As preferências são salvas em `painel_sistema.cfg`, ao lado do executável. Extraia para uma pasta onde você possa gravar, como Documentos. O arquivo pessoal de configuração não é incluído no download. O Windows pode atrasar a abertura no login ou desabilitar a entrada pelo Gerenciador de Tarefas.

O menu de configurações fecha após 5 segundos sem interação (não fecha enquanto o mouse está sobre ele); a janela de seleção de temas permanece aberta até você fechá-la. Use a roda do mouse/barra de rolagem se ele não couber na tela. Sem escolha manual, após 20 segundos o widget resume para círculos (nunca com uma janela de configuração aberta); dois cliques restauram a visão completa e abrem as opções. Clique no X do widget para encerrar.

Telemetria via psutil e sensores disponíveis: valores indisponíveis aparecem como traço. Os testes de distribuição não certificam todos os sensores/hardwares. Nada é enviado para servidores pelo widget. O crédito abre o site no navegador quando clicado.

Desenvolvido por [pablo escobar](https://pabloescobardj.web.app/Wikipedia-Pablo-Escobar.html).

`SHA256SUMS.txt` contém os hashes SHA-256 dos quatro arquivos de distribuição (incluindo version.json).

`version.json` informa a versão e o SHA-256 do executável para a consulta de updates. Publicações anteriores sem esse arquivo são identificadas como sem numeração; o widget não afirma que sejam novas nem que você esteja atualizado. Sem conexão ou sob limite da API, oferece tentar novamente.
