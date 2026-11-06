# 🎯 CS2 Autoexec CFG — JGUILHERME

Configuração personalizada de **Counter-Strike 2 (CS2)**, focada em desempenho, competitividade, precisão e praticidade.

Este `autoexec.cfg` reúne configurações de mouse, mira, HUD, radar, rede, FPS, áudio e atalhos personalizados, permitindo carregar automaticamente todas as preferências ao iniciar o jogo.

---

## 📋 Índice

- [Visão geral](#-visão-geral)
- [Instalação](#-instalação)
- [Opções de inicialização](#-opções-de-inicialização)
- [Mouse e sensibilidade](#-mouse-e-sensibilidade)
- [Mira (Crosshair)](#-mira-crosshair)
- [Sistema de troca de miras](#-sistema-de-troca-de-miras)
- [Viewmodel](#-viewmodel)
- [HUD e interface](#-hud-e-interface)
- [Radar](#-radar)
- [Rede e conexão](#-rede-e-conexão)
- [FPS e desempenho](#-fps-e-desempenho)
- [Áudio](#-áudio)
- [Comportamento geral](#-comportamento-geral)
- [Keybinds](#-keybinds)
- [Salvar configurações](#-salvar-configurações)

---

## 🎮 Visão geral

| Característica | Configuração |
|---|---|
| Jogo | Counter-Strike 2 |
| Arquivo | `autoexec.cfg` |
| Jogador | JGUILHERME |
| Sensibilidade | 2.00 |
| Estilo de mira principal | Amarela |
| Mira alternativa | Cyan |
| FPS máximo | 300 |
| FPS no menu | 143 |
| Viewmodel FOV | 68 |
| Radar | Descentralizado e rotativo |
| Troca de miras | Tecla O |

## 📥 Instalação

1. Abra a pasta de instalação do Steam.
2. Acesse o seguinte diretório:

```text
Steam\userdata\SEU_STEAM_ID\730\local\cfg\
```

3. Crie um arquivo chamado:

```text
autoexec.cfg
```

4. Cole o conteúdo completo da configuração dentro do arquivo.
5. Salve e inicie o CS2.

**Importante:** substitua `SEU_STEAM_ID` pelo identificador correto da sua conta Steam.

## ⚙️ Opções de inicialização

Configuração recomendada para utilizar nas opções de inicialização do CS2:

```text
-novid -nojoy -threads 8 -noaafonts -exec autoexec
```

| Parâmetro | Função |
|---|---|
| `-novid` | Remove o vídeo de introdução. |
| `-nojoy` | Desativa o suporte a joystick. |
| `-threads 8` | Define uma configuração de threads para inicialização. O jogo pode gerenciar isso automaticamente. |
| `-noaafonts` | Parâmetro legado relacionado à suavização de fontes; pode não ter efeito no CS2 atual. |
| `-exec autoexec` | Executa o arquivo autoexec na inicialização. |

## 🖱️ Mouse e sensibilidade

Configurações voltadas à consistência e precisão dos movimentos.

| Comando | Valor | Descrição |
|---|---:|---|
| `sensitivity` | 2.00 | Sensibilidade geral do mouse. |
| `m_pitch` | 0.022 | Multiplicador do movimento vertical. |
| `m_yaw` | 0.022 | Multiplicador do movimento horizontal. |
| `zoom_sensitivity_ratio` | 1.00 | Sensibilidade ao utilizar zoom. |

A sensibilidade é mantida em 2.00 para preservar a consistência da mira.

## 🎯 Mira (Crosshair)

Configuração inicial da mira principal: amarela, estática e sem contorno.

| Comando | Valor | Função |
|---|---:|---|
| `cl_crosshairstyle` | 4 | Define o estilo estático clássico. |
| `cl_crosshairsize` | 6 | Define o tamanho da mira. |
| `cl_crosshairthickness` | 1 | Define a espessura. |
| `cl_crosshairgap` | 4 | Define o espaçamento central. |
| `cl_crosshairalpha` | 255 | Define a opacidade máxima. |
| `cl_crosshaircolor` | 5 | Utiliza cores personalizadas. |
| `cl_crosshaircolor_r` | 255 | Intensidade do vermelho. |
| `cl_crosshaircolor_g` | 255 | Intensidade do verde. |
| `cl_crosshaircolor_b` | 0 | Intensidade do azul. |
| `cl_crosshairdot` | 0 | Desativa o ponto central. |
| `cl_crosshair_drawoutline` | 0 | Desativa o contorno. |
| `cl_crosshair_sniper_width` | 1 | Define a espessura da mira de sniper. |
| `cl_crosshair_recoil` | 0 | Desativa o acompanhamento do recuo pela mira. |

A combinação RGB `255, 255, 0` representa a cor amarela.

## 🔄 Sistema de troca de miras

Um dos recursos personalizados desta CFG é o sistema de alternância de duas miras utilizando apenas uma tecla.

**Tecla utilizada: O**

### Mira 1 — Cyan

- Cor: ciano.
- Estilo: dinâmico.
- Tamanho: 2.
- Espessura: 1.
- Espaçamento: 2.
- Ponto central: ativado.
- Contorno: desativado.

### Mira 2 — Amarela

- Cor: amarelo.
- Estilo: estático.
- Tamanho: 6.
- Espessura: 1.
- Espaçamento: 4.
- Ponto central: desativado.
- Contorno: desativado.

### Como funciona?

O sistema utiliza aliases para alternar automaticamente entre as configurações.

```text
Tecla O
   |
   v
Mira 1 — Cyan
   |
   v
Próximo clique em O
   |
   v
Mira 2 — Amarela
   |
   v
Próximo clique em O
   |
   v
Mira 1 — Cyan
```

A alternância é contínua, sem necessidade de executar comandos manualmente no console.

O sistema também limpa as referências antigas de `mira3` e `mira_3`, evitando conflitos com versões anteriores da configuração.

## 🔫 Viewmodel

Define a posição e o campo de visão da arma na tela.

| Comando | Valor | Função |
|---|---:|---|
| `viewmodel_fov` | 68 | Campo de visão da arma. |
| `viewmodel_offset_x` | 2.5 | Posicionamento horizontal. |
| `viewmodel_offset_y` | 0 | Posicionamento de profundidade. |
| `viewmodel_offset_z` | -1.5 | Posicionamento vertical. |
| `viewmodel_presetpos` | 1 | Preset de posicionamento. |
| `cl_prefer_lefthanded` | 0 | Mantém a arma na mão direita. |
| `fov_desired` | 75 | Valor de FOV desejado, sujeito às limitações do CS2. |

Objetivo: manter uma visualização confortável, liberando espaço na tela para acompanhar melhor os adversários.

## 🖥️ HUD e interface

Personalização dos elementos visuais durante as partidas.

| Comando | Valor | Função |
|---|---:|---|
| `hud_scaling` | 1.0 | Escala da interface. |
| `safezonex` | 0.9 | Ajuste horizontal da área segura. |
| `safezoney` | 0.9 | Ajuste vertical da área segura. |
| `cl_hud_color` | 3 | Cor da interface. |
| `hud_showtargetid` | 1 | Exibe identificação do jogador observado. |
| `cl_showloadout` | 1 | Mantém o inventário visível. |
| `cl_hud_radar_scale` | 1.0 | Escala dos elementos do radar no HUD. |

### Telemetria

A CFG também habilita indicadores de desempenho e conexão:

- `cl_hud_telemetry_frametime_show 2`: exibição de frametime.
- `cl_hud_telemetry_ping_show 1`: exibição de ping.
- `cl_hud_telemetry_net_misdelivery_show 1`: exibição de problemas de entrega de pacotes.

Esses indicadores ajudam a identificar possíveis problemas de desempenho e conexão durante as partidas.

## 🗺️ Radar

Configuração voltada à visualização de uma área maior do mapa.

| Comando | Valor | Função |
|---|---:|---|
| `cl_radar_scale` | 0.4 | Zoom do radar. |
| `cl_radar_always_centered` | 0 | Permite visualizar mais do mapa. |
| `cl_radar_rotate` | 1 | Radar acompanha a direção do jogador. |
| `cl_radar_icon_scale_min` | 0.6 | Tamanho mínimo dos ícones. |
| `cl_radar_square_always` | 0 | Mantém o formato circular. |

### Alternância de zoom

A tecla **Q** alterna entre dois níveis de zoom:

- `1`: aproximação.
- `0.4`: visualização ampliada.

Facilita a leitura do mapa em diferentes situações.

## 🌐 Rede e conexão

Configurações relacionadas à comunicação com os servidores.

| Comando | Valor | Função |
|---|---:|---|
| `rate` | 786432 | Limite de taxa de transferência de dados. |
| `cl_net_buffer_ticks` | 0 | Configuração do buffer de rede. |
| `mm_dedicated_search_maxping` | 55 | Ping máximo desejado na busca de servidores. |

O objetivo é manter uma conexão responsiva e evitar a busca por servidores com latência muito elevada.

## 🚀 FPS e desempenho

Limites de FPS e configurações voltadas à redução de processamento visual desnecessário.

| Comando | Valor | Função |
|---|---:|---|
| `fps_max` | 300 | Limite de FPS durante o jogo. |
| `fps_max_ui` | 143 | Limite de FPS nos menus. |
| `cl_ragdoll_limit` | 0 | Tentativa de limitar a quantidade de ragdolls. |
| `cl_predict_kill_ragdolls` | 0 | Configuração relacionada à previsão de ragdolls. |
| `func_break_max_pieces` | 0 | Limita fragmentos de objetos quebráveis. |
| `enable_boneflex` | 0 | Configuração de animações de flexão dos modelos. |
| `r_drawtracers_firstperson` | 1 | Mantém os rastros de tiros em primeira pessoa. |

**Observação:** alguns comandos de desempenho são legados, experimentais ou podem não ser reconhecidos pelas versões atuais do CS2. O jogo pode ignorá-los, e sua presença não garante aumento de FPS. O desempenho real depende principalmente do hardware e das configurações gráficas.

## 🔊 Áudio

Configuração de volume geral, comunicação e efeitos sonoros.

| Categoria | Configuração |
|---|---|
| Volume geral | 0.303292 |
| Volume do jogo | 1.0 |
| Voz dos jogadores | 1.0 |
| Comunicação por voz | 1.0 |
| Música | 1.0 |
| Música do menu | 0 |
| Música de MVP | 0 |
| Som de fim de round | 0 |
| Som de início de round | 0 |
| Som de ação do round | 0 |
| Câmera de morte | 0 |
| Objetivos do mapa | 0 |
| Aviso de 10 segundos | 0.04 |

Outras configurações:

- `snd_mute_losefocus 1`: silencia o jogo quando perde o foco da janela.
- `voice_vox 0`: desativa o modo de ativação de voz por detecção automática.

A intenção é priorizar os sons importantes da partida, reduzindo músicas e notificações desnecessárias.

## ⚙️ Comportamento geral

| Comando | Valor | Função |
|---|---:|---|
| `con_enable` | 1 | Habilita o console. |
| `cl_use_opens_buy_menu` | 0 | Desativa a abertura do menu de compra pelo uso. |
| `cl_silencer_mode` | 1 | Configuração do comportamento do silenciador. |
| `cl_sniper_auto_rezoom` | 1 | Ativa o zoom automático após disparos de sniper. |
| `cl_sniper_show_inaccuracy` | 0 | Oculta o indicador de imprecisão da sniper. |
| `cl_weapon_selection_rarity_color` | 1 | Ativa cores de raridade na seleção de armas. |
| `cl_allow_animated_avatars` | 0 | Desativa avatares animados. |
| `cl_player_ping_mute` | 1 | Configuração de silenciamento de pings de jogadores. |

## ⌨️ Keybinds

Atalhos personalizados para facilitar as ações durante as partidas.

| Tecla | Ação |
|---|---|
| `V` | Comunicação por voz. |
| `MOUSE1` | Atirar. |
| `MOUSE4` | Granada flash. |
| `MOUSE5` | Granada de fumaça. |
| `MWHEELUP` | Pular. |
| `MWHEELDOWN` | Pular. |
| `SPACE` | Pular. |
| `Q` | Alternar zoom do radar. |
| `O` | Alternar entre as duas miras. |
| `P` | Comprar conjunto de armas (autobuy). |
| `F` | Inspecionar arma. |
| `Z` | Menu de comandos de rádio. |
| `ALT` | Noclip (quando permitido). |
| `CAPSLOCK` | Ping do jogador. |
| `` ` `` | Abrir/fechar console. |

### Observações sobre os atalhos

- `MOUSE4` e `MOUSE5` utilizam os slots 7 e 8, respectivamente.
- `ALT` utiliza o comando `noclip`, que depende das permissões do servidor e normalmente funciona em partidas locais com cheats habilitados.
- O bind de Jumpthrow está desativado por padrão.

## 💾 Salvar configurações

Ao final do arquivo existe:

```cfg
host_writeconfig
```

Esse comando solicita ao CS2 que grave as configurações atuais no arquivo de configuração.

---

## 🛠️ Personalização

O arquivo foi estruturado em blocos independentes para facilitar futuras alterações.

É possível modificar individualmente:

- Sensibilidade do mouse.
- Cores, tamanho e estilo das miras.
- Posição da arma.
- Escala e zoom do radar.
- Limites de FPS.
- Volumes de áudio.
- Teclas de atalho.

Para atualizar a configuração, basta editar o `autoexec.cfg` e executar no console:

```cfg
exec autoexec
```

## ⚠️ Compatibilidade

Esta configuração foi criada para o Counter-Strike 2.

Comandos podem ser modificados, removidos ou bloqueados em atualizações do jogo. Caso algum comando deixe de funcionar, verifique sua disponibilidade no console do CS2.

**Objetivo do projeto:** manter uma configuração pessoal, organizada, documentada e de fácil manutenção, reunindo os principais ajustes competitivos em um único arquivo.

---

**Autor:** JGUILHERME

**Projeto:** CS2 Autoexec CFG

**Tecnologia:** Counter-Strike 2 / Source 2

**Formato:** `.cfg`
