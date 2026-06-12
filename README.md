# Amphi🛡️ Amphi: The Black Box
The Autonomous Immune System for Critical Infrastructures | O Sistema Imunológico Autônomo para Infraestruturas Críticas
Amphi Logo

📑 Índice (Table of Contents)
A Visão (The Vision)
Arquitetura (Architecture)
Inteligência em Enxame (Swarm Intelligence)
Pré-requisitos (Prerequisites)
Instalação e Quick Start
Roadmap
Como Contribuir (Contributing)
📖 A Visão (The Vision)
💡 The Origin & Vision | A Origem e a Visão [EN] The Origin Story: The idea for Amphi was born from the observation of a paradox: our digital systems are the backbone of modern civilization, yet they remain incredibly fragile. Traditional security is static, relying on walls that are perpetually bypassed by AI-driven threats. I realized that if we want to secure the future, we must stop building "walls" and start growing "organisms."

[PT-BR] A Origem da Ideia: A ideia do Amphi nasceu da observação de um paradoxo: nossos sistemas digitais são a espinha dorsal da civilização moderna, mas permanecem incrivelmente frágeis. A segurança tradicional é estática, baseada em muros que são perpetuamente contornados por ameaças movidas por IA. Percebi que, se queremos proteger o futuro, precisamos parar de construir "muros" e começar a cultivar "organismos".

🧬 Why the Name "Amphi"? | Por que o nome "Amphi"?
[EN] The Meaning: The name is derived from the prefix "Amphi-" (from Ancient Greek amphi), meaning "both," "on both sides," or "surrounding."

Bio-mimicry: It represents an Amphibian nature—the ability to adapt and survive in two different environments: the User-Space (where applications run) and the Kernel-Space (where the system breathes).

Security: Like an amphibian that thrives in water and on land, Amphi thrives within the deep kernel and the high-level network topology, providing "surrounding" protection that is both internal and external.

[PT-BR] O Significado: O nome deriva do prefixo "Amphi-" (do grego antigo amphi), que significa "ambos", "de ambos os lados" ou "ao redor".

Bio-mimetismo: Representa uma natureza Anfíbia — a capacidade de se adaptar e sobreviver em dois ambientes distintos: o User-Space (onde as aplicações rodam) e o Kernel-Space (onde o sistema respira).

Segurança: Assim como um anfíbio que prospera na água e na terra, o Amphi prospera nas profundezas do kernel e na topologia de rede de alto nível, fornecendo uma proteção "ao redor" que é, simultaneamente, interna e externa.

🧠 Why This Architecture? | Por que esta arquitetura?
[EN] The Concept: Most security solutions are reactive (they wait for an attack signature). Amphi is proactive and cognitive. By using eBPF, we gain an "omnipresent view" of the system without performance loss. By using Mojo, we achieve the speed of C with the intelligence of modern AI, allowing the system to learn the difference between a "normal user" and a "malicious threat" in real-time.

[PT-BR] O Conceito: A maioria das soluções de segurança é reativa (esperam por uma assinatura de ataque). O Amphi é proativo e cognitivo. Ao usar eBPF, ganhamos uma "visão onipresente" do sistema sem perda de performance. Ao usar Mojo, alcançamos a velocidade de C com a inteligência da IA moderna, permitindo que o sistema aprenda a diferença entre um "usuário normal" e uma "ameaça maliciosa" em tempo real.

[EN] Market Value: This roadmap transforms Amphi from a simple "Antivirus" into an Autonomous Security Analyst, drastically reducing operational costs (OpEx) for SOC teams and meeting the highest global regulatory standards (NIS2, GDPR, SOX).

[PT-BR] Valor de Mercado: Este roadmap transforma o Amphi de um simples "Antivírus" em um Analista de Segurança Autônomo, reduzindo drasticamente os custos operacionais (OpEx) de equipes de SOC e atendendo aos mais altos padrões regulatórios globais (NIS2, GDPR, SOX).
[EN] Competitive Positioning
Amphi transcends traditional security by shifting from reactive detection to Cognitive Intent Analysis and Hardened Autonomy.

Brain (Mojo): From Detection to Intent By utilizing Inverse Reinforcement Learning (IRL), the Brain doesn't just identify "what" a process is doing; it predicts "why" it is doing it. By forecasting an adversary’s next three moves, Amphi intercepts attacks before they fully manifest.
Fail-Closed: Mathematical Integrity We move beyond logic to physical security by anchoring our Fail-Closed mechanism to Hardware Root of Trust (TPM 2.0/HSM). If the Amphi agent is tampered with, the system triggers a hardware-level lock, rendering the node unreachable to unauthorized entities.
[PT-BR] Posicionamento Competitivo
O Amphi transcende a segurança tradicional, migrando da detecção reativa para a Análise Cognitiva de Intenção e Autonomia Blindada.

Brain (Mojo): Da Detecção à Intenção Utilizando Aprendizado por Reforço Inverso (IRL), o Brain não apenas identifica "o que" um processo está fazendo; ele prevê o "porquê". Ao antecipar os próximos três passos de um adversário, o Amphi intercepta ataques antes que eles se concretizem.
Fail-Closed: Integridade Matemática Elevamos a segurança da lógica para o hardware, ancorando nosso mecanismo Fail-Closed em uma Raiz de Confiança por Hardware (TPM 2.0/HSM). Caso o agente Amphi seja adulterado, o sistema aciona um travamento em nível de hardware, tornando o nó inacessível para entidades não autorizadas.
🗺️ Startup Roadmap / Roadmap de Desenvolvimento
Stage	Focus	Objective
Phase 1 (MVP)	eBPF Observability	Sell "Amphi Insight": total visibility with zero latency.
Phase 2 (Scale)	Rust Enforcer	Add autonomous containment capabilities via Cgroups.
Phase 3 (Cognitive)	Mojo Brain	Deliver proactive behavioral Zero-Day detection.
Phase 4 (Federated)	Swarm Intelligence	Monetize collective defense through ecosystem-wide learning.
⚙️ Pré-requisitos
Como o Amphi opera no nível mais profundo do sistema operacional, o ambiente hospedeiro precisa atender a alguns requisitos mínimos:

OS: Linux (Arch Linux, Ubuntu 22.04+, ou qualquer distribuição com suporte nativo a eBPF)
Kernel: Linux Kernel versão 5.8 ou superior (necessário para os hooks avançados do eBPF).
Dependências de Build:
Rust (cargo e rustc 1.70+)
Go (1.20+)
Clang/LLVM (para compilar os programas eBPF em C)
Node.js / TypeScript (para a engine do Memory/Forensics)
Python (3.10+)
🏛️ Detalhamento da Arquitetura (Deep Dive)
O Amphi funciona como um organismo composto por sete especializações tecnológicas (órgãos), cada uma focada em uma função crítica de sobrevivência:

1. Nerves (eBPF / C) – A Percepção
Função: Monitoramento ininterrupto de eventos de kernel (Syscalls, Networking, Disk I/O).
Por que: É a única forma de obter visibilidade total sem injetar latência. O eBPF permite que o Amphi "sinta" o que está acontecendo sem que o invasor consiga mascarar sua presença através de bibliotecas de usuário (user-space hooks).
2. Filter (C++) – O Sistema Límbico
Função: Processamento de sinais brutos e redução de ruído.
Por que: O kernel gera milhões de eventos por segundo. O C++ é o "filtro" que descarta o tráfego legítimo (ruído) e passa apenas as anomalias relevantes para a IA. É a camada de alta performance que garante que o "cérebro" não sofra sobrecarga.
3. Brain (Mojo) – A Cognição Adaptativa
Função: Inferência preditiva baseada em comportamento (Behavioral Analysis).
Por que: Diferente de firewalls que buscam por "assinaturas de vírus" (conhecimento passado), o motor Mojo analisa a intenção (conhecimento presente). Se um processo começa a ler arquivos de sistema que nunca acessou, o Mojo classifica aquilo como anomalia de comportamento, detectando ataques Zero-Day que nenhuma lista de bloqueio conseguiria prever.
4. Enforcer (Rust) – A Resposta Imunológica
Função: Isolamento, bloqueio e mitigação.
Por que: Em uma emergência, falhas de software são inaceitáveis. O Rust garante que as ações de defesa (kill, block, isolate) sejam executadas com Memory Safety. O sistema de defesa nunca derrubará o servidor por um erro de segmentação (Memory Leak/Segmentation Fault).
5. Memory (TS / SQL) – O Registro Forense (The Black Box)
Função: Armazenamento de estado, reconstrução de incidentes e análise histórica.
Por que: Esta é a "Caixa-Preta" do avião. Ela não apenas grava logs; ela armazena snapshots de memória e o contexto completo da rede no momento da invasão. Isso permite o Digital Twin Playback: você pode simular a invasão novamente em ambiente fechado para estudar o exploit.
6. Ghost (Go / Envoy) – A Decepção Estratégica (MTD)
Função: Moving Target Defense (MTD) e Honeypots dinâmicos.
Por que: A melhor defesa é fazer o atacante perder tempo. O Amphi rotaciona portas e rotas de serviço dinamicamente. O atacante acha que está explorando um alvo, mas está sendo guiado para uma armadilha (Sandbox), enquanto o serviço real está "em outro lugar" na topologia da rede.
7. Orchestrator (Python) – O Sistema Nervoso Central
Função: Agregação de telemetria, injeção dinâmica de políticas, controle de automação e integração externa (Glue-Code).
Por que: Enquanto Rust e C/eBPF controlam os "reflexos" mecânicos e instantâneos do sistema, o Python opera como a mente consciente para gerenciamento estratégico. Ele unifica os órgãos do Amphi, facilitando a automação de ferramentas forenses, orquestração do Modo Caos e integração nativa com SIEMs (Splunk, ELK) e APIs de nuvem sem comprometer o caminho crítico de baixa latência.
🌐 Encrypted Traffic Vision | Visão de Tráfego Encriptado
[EN] Modern ransomware and data exfiltration malware heavily leverage TLS 1.3 or QUIC protocols, rendering traditional kernel-space eBPF inspection (XDP/TC) blind to the encrypted payloads. To bypass this limitation, the Nerves module implements user-space dynamic tracing via uprobes and uretprobes. By anchoring directly into the runtime memory of cryptographic libraries like OpenSSL and BoringSSL (specifically targeting SSL_read and SSL_write), Amphi intercepts and reads the raw plaintext payload a millisecond before encryption occurs and the packet hits the network interface. This achieves 100% visibility into malicious payloads without the overhead of a decryption proxy or the need to break mutual TLS (mTLS).
[PT-BR] Ransomwares modernos e malwares de exfiltração utilizam intensamente os protocolos TLS 1.3 ou QUIC, tornando a inspeção tradicional de eBPF no kernel-space (XDP/TC) cega para pacotes criptografados. Para superar essa limitação, o módulo Nerves implementa rastreamento dinâmico em user-space via uprobes e uretprobes. Ao ancorar-se diretamente na memória de execução de bibliotecas criptográficas como OpenSSL e BoringSSL (visando especificamente as funções SSL_read e SSL_write), o Amphi intercepta e lê o payload em texto plano um milissegundo antes da criptografia acontecer e o pacote ser enviado para a interface de rede. Isso garante visibilidade total contra tráfego malicioso sem o overhead de um proxy de interceptação ou a necessidade de quebrar o mTLS.
⏳ Micro-Segmentation & Throttling | Micro-segmentação e Estrangulamento
[EN] Immediately terminating a compromised process (SIGKILL) alerts an advanced adversary that their presence has been discovered, triggering automated evasion or anti-forensics measures. The Enforcer module addresses this by leveraging Linux Cgroups v2 for silent, dynamic throttling. Instead of killing or freezing the thread, the Rust agent seamlessly migrates the malicious process into a highly restricted, isolated cgroup namespace. Here, it slashes the process's CPU quota (e.g., down to 1%) and heavily constrains its disk I/O bandwidth (IOPS). The malware continues executing, but at such an agonizingly slow velocity that a ransomware attack that would normally destroy a disk in seconds now takes years to complete, buying infinite time for the forensics engine to capture live memory states.
[PT-BR] Matar imediatamente um processo comprometido (SIGKILL) alerta um adversário avançado de que sua presença foi descoberta, disparando contramedidas automatizadas de evasão ou anti-forense. O módulo Enforcer resolve isso utilizando o Cgroups v2 do Linux para realizar um estrangulamento silencioso e dinâmico. Em vez de derrubar ou congelar a thread, o agente em Rust migra perfeitamente o processo malicioso para um namespace isolado e altamente restrito do cgroup. Nele, o sistema corta a cota de CPU do processo (ex: para 1%) e restringe severamente a banda de I/O de disco (IOPS). O malware continua rodando, mas a uma velocidade tão ínfima que um ataque de ransomware que destruiria o disco em segundos passa a levar anos, garantindo tempo infinito para o motor forense capturar estados de memória viva.
⚡ Side-Channel & Hardware Monitoring | Monitoramento de Side-Channel por Hardware
[EN] Highly sophisticated exploits (such as Spectre, Meltdown, or stealthy, low-footprint cryptominers) often leave no footprints in traditional network connections or standard disk I/O syscalls. To detect these microscopic vectors, Amphi bridges its eBPF subsystem with the Linux perf_events API to continuously sample Hardware Performance Counters (PMCs) directly from the CPU. The system monitors core microarchitectural metrics including L1/L2/L3 Cache Misses, Branch Prediction Failures, and Instructions Per Cycle (IPC) anomalies. If a seemingly benign or legitimate user-space application begins to induce rhythmic cache misses or abnormal branch mispredictions, the Brain (Mojo) immediately correlates the hardware telemetry to isolate the hardware side-channel attack in real-time.
[PT-BR] Exploits extremamente sofisticados (como Spectre, Meltdown ou cryptominers furtivos de baixo consumo) frequentemente não deixam pegadas em conexões de rede ou chamadas de sistema padrão de I/O de disco. Para detectar esses vetores microscópicos, o Amphi conecta seu subsistema eBPF com a API perf_events do Linux para amostrar continuamente os Hardware Performance Counters (PMCs) diretamente da CPU. O sistema monitora métricas microarquiteturais críticas, incluindo Cache Misses (L1/L2/L3), falhas de predição de desvio (Branch Prediction Failures) e anomalias de Instruções por Ciclo (IPC). Se uma aplicação aparentemente legítima em user-space começa a induzir falhas rítmicas de cache ou desvios anômalos, o Brain (Mojo) correlaciona a telemetria de hardware para isolar o ataque de canal lateral em tempo real.
🛡️ Swarm Differential Privacy | Privacidade Diferencial no Enxame
[EN] When sharing behavioral threat signatures ("vaccines") across the Federated Swarm Ecosystem, there is an inherent risk of accidentally leaking sensitive application runtime data, memory configurations, or payload fragments from the initially targeted server. Amphi mitigates this privacy vector by executing a localized Differential Privacy (DP) mathematical algorithm before broadcasting any telemetry to the cluster. The node injects calculated statistical noise into the threat vector, mathematically masking any Personally Identifiable Information (PII), keys, or confidential customer data. This ensures that while the exact, unique cryptographic and behavioral pattern of the malware is perfectly preserved for collective defense, the host node identity and context remain completely unrecoverable, fulfilling strict Zero-Trust compliance.
[PT-BR] Ao compartilhar vacinas comportamentais contra ameaças (assinaturas de ataque) por todo o Ecossistema Federado, existe o risco inerente de vazar acidentalmente dados sensíveis de execução, configurações de memória ou fragmentos de payload do servidor inicialmente atacado. O Amphi mitiga esse vetor de privacidade executando um algoritmo matemático de Privacidade Diferencial (DP) local antes de transmitir qualquer telemetria ao cluster. O nó injeta um ruído estatístico calculado no vetor da ameaça, mascarando matematicamente qualquer Informação de Identificação Pessoal (PII), chaves ou dados confidenciais do cliente. Isso garante que, enquanto o padrão comportamental e criptográfico exato do malware é preservado para a defesa coletiva, o contexto e a identidade do nó de origem permanecem irrecuperáveis, cumprindo regras estritas de conformidade Zero-Trust.
🧪 Continuous Auto-Audit (Chaos Mode) | Auto-Auditoria Contínua (Modo Caos)
[EN] To guarantee that the system's autonomous immunological defenses remain functional and un-tampered during prolonged operational periods without real-world security incidents, Amphi introduces a continuous Chaos Engineering submodule. During designated low-traffic, low-risk infrastructure windows, this module safely injects non-destructive, synthetic pseudo-malware processes into the runtime environment. These automated agents attempt to simulate common adversarial actions, such as reading restricted system configurations or spawning unauthorized reverse shells. This continuously tests if the eBPF kernel hooks, user-space uprobes, and Ghost (MTD) deceptive honey-ports are active and responsive, generating a real-time "Immunological Health Score" directly on the central dashboard.
[PT-BR] Para garantir que as defesas imunológicas autônomas do sistema permaneçam totalmente operacionais e invioladas durante longos períodos operacionais sem incidentes reais de segurança, o Amphi introduz um submódulo contínuo de Chaos Engineering. Durante janelas designadas de baixo tráfego e baixo risco na infraestrutura, este módulo injeta de forma segura processos sintéticos não-destrutivos (pseudomalwares) no ambiente de runtime. Esses agentes automatizados tentam simular ações adversárias comuns, como a leitura de configurações restritas do sistema ou a criação de shells reversas não autorizadas. Isso testa continuamente se os hooks de eBPF no kernel, as uprobes em user-space e as portas falsas do Ghost (MTD) estão ativos e responsivos, gerando um "Score de Saúde Imunológica" em tempo real diretamente no dashboard central.
🛡️ Casos de Uso na Prática (The Amphi in Action)
Ransomware Zero-Day: Um ransomware desconhecido tenta encriptar o disco. O Brain (Mojo) detecta uma anomalia na taxa de IOPS e syscalls de escrita não naturais. O Enforcer (Rust) congela o processo em microssegundos antes que o primeiro arquivo seja corrompido.
Vazamento de Dados (Exfiltration): Um atacante compromete uma aplicação web e tenta enviar dados para um IP na Rússia. O Nerves (eBPF) detecta o socket anômalo. O Ghost (Go/Envoy) intercepta a conexão e redireciona o tráfego do atacante para um Honeypot, fazendo-o acreditar que o download está acontecendo, enquanto o time de segurança é alertado.
🛡️ Amphi: Operational Lifecycle & Control
🛡️ Amphi: Ciclo de Vida Operacional e Controle
1. Initialization Workflow | Fluxo de Inicialização (amphi start)
[EN] When you execute amphi start, the system executes three security layers in milliseconds:

Bootstrapping (Integrity Check): Verifies kernel flags for eBPF and ensures required modules (bpf_prog) can be loaded.
Data Plane Injection: The Rust agent injects compiled .o (eBPF) objects directly into kernel hooks (XDP for network, Tracepoints for syscalls).
Swarm Synchronization: Connects your node to the Federated Ecosystem to fetch the latest "vaccines" (security patterns).
[PT-BR] Quando você executa amphi start, o sistema executa três camadas de segurança em milissegundos:

Bootstrapping (Verificação de Integridade): Verifica as flags do Kernel para eBPF e garante que os módulos necessários (bpf_prog) possam ser carregados.
Injeção do Data Plane: O agente em Rust injeta os objetos compilados .o (eBPF) diretamente nos hooks do kernel (XDP para rede, Tracepoints para syscalls).
Sincronização do Enxame: Conecta seu nó ao Ecossistema Federado para buscar as "vacinas" (padrões de segurança) mais recentes.
2. Cluster Connectivity | Conectividade de Cluster (amphi connect)
[EN] Transforms an isolated server into a Collective Intelligence Node.

Authentication: Uses mutual TLS (mTLS) to secure communication with the cluster or private dashboard.
Heartbeat: Establishes a constant telemetry channel, sending full exploit context, not just raw logs.
[PT-BR] Transforma um servidor isolado em um Nó de Inteligência Coletiva.

Autenticação: Utiliza mTLS (Mutual TLS) para garantir uma comunicação segura com o cluster ou painel de controle privado.
Heartbeat: Estabelece um canal de telemetria constante, enviando o contexto completo do exploit, não apenas logs brutos.
3. Operational States | Estados Operacionais
[EN] Because Amphi is active kernel-level security, stopping it requires specific states to maintain system integrity. [PT-BR] Como o Amphi é uma segurança ativa ao nível do Kernel, parar o sistema exige estados específicos para manter a integridade do sistema.

Command	Kernel State (eBPF)	AI State (Brain)	Logs (Black Box)
pause	Active (Monitoring)	Disabled	Active (Logging)
stop	Detached (Removed)	Disabled	Inactive
shutdown	Removed + Cleaned	Disabled	Removed
Definitions | Definições
amphi pause: Use for maintenance (e.g., patching). It stops blocking/analysis but keeps monitoring active.
amphi stop: Shuts down the agent and detaches all BPF probes.
amphi shutdown: Total de-installation. Clears all BPF Maps and forensics cache. Requires secondary authentication if auto-repair is active.
amphi pause: Use para manutenção (ex: atualizar o sistema). Interrompe bloqueios e análises, mas mantém o monitoramento passivo.
amphi stop: Encerra o agente e desanexa todas as sondas BPF.
amphi shutdown: Desinstalação total. Limpa todos os BPF Maps e o cache forense. Exige autenticação secundária se o auto-reparo estiver ativo.
Amphi CLI Ecosystem / Ecossistema de CLI Amphi
1. Vital Signs / Sinais Vitais e Diagnóstico
EN
Real-time health metrics to ensure the system runtime is coherent and un-tampered.

amphi status Returns a high-level telemetry dashboard. (e.g., "Immunological Health: 98% | Blocked Threats: 4 | eBPF Hook Latency: 0.02ms").
amphi pulse Cryptographically verifies the real-time heartbeat synchronization between the user-space agent and low-level kernel hooks.
amphi audit Compiles a structural report of recent system modifications and historical blocks ("scar logs"), designed for strict compliance audits.
PT-BR
Métricas de saúde em tempo real para garantir que a execução do sistema esteja coerente e livre de adulterações.

amphi status Retorna um dashboard rápido de telemetria. (Ex: "Saúde Imunológica: 98% | Ameaças Bloqueadas: 4 | Latência do Hook eBPF: 0.02ms").
amphi pulse Verifica criptograficamente a sincronização do batimento cardíaco (heartbeat) entre o agente em user-space e os hooks de baixo nível no kernel.
amphi audit Compila um relatório estrutural de modificações recentes no sistema e históricos de bloqueio ("logs de cicatrizes"), ideal para auditorias estritas de conformidade.
2. Immune Response / Resposta Imunológica Ativa
EN
Manual overrides to force behavioral containment and collective swarm updates.

amphi vaccinate <threat_id> Forces the immediate pull of a specific threat signature vector from the cluster network or broadcasts a locally generated threat profile to the Federated Swarm.
amphi isolate <PID> Direct manual intervention. Instantly migrates a suspicious Process ID into the highly constrained, throttled Linux Cgroups v2 sandbox namespace.
amphi simulate <type> Triggers the continuous Chaos Engineering submodule manually to test specific active defense vectors (e.g., amphi simulate ransomware or amphi simulate ddos).
PT-BR
Substituições manuais para forçar a contenção comportamental e atualizações coletivas do enxame.

amphi vaccinate <threat_id> Força o download imediato de um vetor de assinatura de ameaça específico da rede do cluster ou transmite um perfil de ameaça gerado localmente para o Enxame Federado.
amphi isolate <PID> Intervenção manual direta. Migra instantaneamente um Process ID suspeito para o namespace isolado e severamente limitado do Linux Cgroups v2.
amphi simulate <type> Ativa o submódulo de Chaos Engineering de forma manual para testar vetores de defesa ativos específicos (Ex: amphi simulate ransomware ou amphi simulate ddos).
3. Nervous System / Configuração e Políticas (System Overlays)
EN
Fine-tuning adaptive operational modes without disrupting critical data-plane traffic.

amphi config --reload Dynamically reloads the amphi.yaml rules manifest with absolute zero downtime, updating active filter meshes instantly.
amphi swarm-join <token> Authenticates and binds the current node into the local or global cluster, enabling decentralized P2P threat vector updates.
amphi policy --set <mode> Shifts global defense logic behavior profile:
paranoid: Maximum enforcement. Immediate isolation and lock on any micro-architectural or network anomaly.
balanced: Standard behavioral operation. Mitigation triggers rely on high-confidence Mojo AI classification score.
learning: Passive observation mesh. Tracks anomalies, registers logs, but strictly drops blocking actions.
PT-BR
Ajuste fino de modos operacionais adaptativos sem interromper o tráfego crítico do plano de dados.

amphi config --reload Recarrega dinamicamente o manifesto de regras amphi.yaml com zero downtime absoluto, aumentando as malhas de filtragem ativas instantaneamente.
amphi swarm-join <token> Autentica e vincula o nó atual ao cluster local ou global, habilitando atualizações descentralizadas de vetores de ameaça via P2P.
amphi policy --set <mode> Alterna o perfil global de comportamento de defesa:
paranoid: Execução máxima. Isolamento imediato e travamento ante qualquer anomalia de rede ou microarquitetural.
balanced: Operação comportamental padrão. Mitigações dependem de um score de alta confiança da IA (Mojo).
learning: Malha de observação passiva. Rastreia anomalias e registra logs, mas não executa bloqueios.
4. Forensics / Investigação da Caixa-Preta (Black Box)
EN
Extracting contextual infrastructure footprints following a targeted malicious incident.

amphi dump <incident_id> Exports a highly secure, isolated execution memory snapshot and the historical network state captured at the exact microsecond of the breach.
amphi replay <incident_id> Spawns a secure Digital Twin sandbox topology to replay the recorded exploit footprint, mapping out precise adversarial methods.
PT-BR
Extração de pegadas contextuais da infraestrutura após um incidente malicioso direcionado.

amphi dump <incident_id> Exporta um snapshot altamente seguro e isolado da memória de execução e do estado histórico da rede capturado no microssegundo exato da invasão.
amphi replay <incident_id> Cria uma topologia sandbox segura de Gêmeo Digital (Digital Twin) para reproduzir o exploit gravado, mapeando os métodos precisos do adversário.
5. Command Matrix Summary / Resumo Estruturado de Comandos
Category / Categoria	Command / Comando	Action (EN)	Ação (PT-BR)
Status	amphi status	Real-time node structural telemetry & health scoreboard.	Telemetria estrutural e score de saúde do nó em tempo real.
Control / Controle	amphi policy	Dynamically alters active runtime enforcement logic (learning, balanced, paranoid).	Altera dinamicamente as regras de execução ativa em runtime.
Response / Resposta	amphi isolate	Forces immediate automated process migration into the containment cgroup.	Força a migração imediata de um processo para o cgroup de contenção.
Swarm / Enxame	amphi vaccinate	Syncs behavioral vaccine profiles and rules across the decentralized P2P cluster.	Sincroniza perfis de vacinas comportamentais com o cluster P2P descentralizado.
Forensics / Forense	amphi dump	Extracts secure memory snapshot and historical network state at the breach microsecond.	Exporta um snapshot de memória e o estado histórico da rede no microssegundo da invasão.
⚠️ Engineering Note | Nota de Engenharia
[EN] Implement a systemd watchdog. If Amphi is stopped without authorization or terminated by malware, the system should trigger a Fail-Closed (network lock) and alert the central dashboard.

[PT-BR] Implemente um systemd watchdog. Se o Amphi for parado sem autorização ou finalizado por malware, o sistema deve acionar um Fail-Closed (travamento de rede) e alertar o painel central imediatamente.

🧬 Inteligência em Enxame (Swarm Intelligence)
O Amphi não é apenas local; ele é um Ecossistema Federado.

Aprendizado Federado: Cada nó (servidor) é um estudante. Quando o nó A aprende que uma sequência de pacotes específica é um ataque, ele cria uma "vacina" (um vetor de detecção). Essa vacina é compartilhada via protocolo de rede com todos os outros nós do cluster.

Imunidade de Rebanho: Uma ameaça detectada em um servidor da ponta torna todo o seu Data Center imune a ela em segundos. O atacante nunca terá sucesso duas vezes.

Auto-Reparação (Self-Healing): Se o Amphi detecta um processo comprometido, ele não apenas bloqueia; ele rotaciona segredos (API Keys, tokens), reinicia os contêineres a partir de uma imagem limpa e notifica o painel central, tudo isso sem intervenção humana.

⚖️ Architectural Risks & Mitigations | Riscos Arquiteturais e Mitigações
1. "Security by Excess" Risk (Kernel Instability) | O Risco de "Segurança por Excesso" (Instabilidade do Kernel)
[EN] Risk: Operating deep within kernel-space using eBPF hooks poses a theoretical risk of causing a Kernel Panic (completely crashing the system) if logic errors, unauthorized memory access, or infinite loops occur in the bpf_prog.
[EN] Mitigation: Amphi builds completely upon the mathematical guarantees of the Linux platform's native BPF Verifier. Before any code is loaded into the kernel, the verifier acts as a strict static analyzer that completely rejects unsafe memory paths, uninitialized variables, or unbounded loops, making runtime kernel crashes structurally impossible.
[PT-BR] Risco: O uso de eBPF e hooks no Kernel pode causar um Kernel Panic (o sistema trava completamente) se o seu código tiver um erro de lógica, acesso indevido à memória ou um laço infinito no bpf_prog.
[PT-BR] Mitigação: O Amphi é construído totalmente sobre as garantias matemáticas do BPF Verifier nativo da plataforma Linux. Antes que qualquer código seja carregado no kernel, o verificador impede que código inseguro ou que possa travar o sistema seja inserido, garantindo a estabilidade operacional da própria plataforma.
2. Performance Overhead (Latency vs. Protection) | Overhead de Performance (Latência vs. Proteção)
[EN] Risk: Even though eBPF runs at near-native hardware speed, continuous monitoring of intensive system-wide syscalls and heavy user-space uprobe tracing on cryptographic libraries (like OpenSSL) can degrade host application performance under maximum throughput conditions.
[EN] Mitigation: The C++ Filter module is designed exactly as an ultra-fast triage layer to eliminate noise at line-rate. Only telemetry that passes this localized pre-classification is offloaded to the complex AI engine (Mojo), keeping the main execution hot-path overhead effectively close to zero.
[PT-BR] Risco: Embora o eBPF seja extremamente rápido, o monitoramento constante de syscalls, especialmente com inspeção de uprobes em bibliotecas criptográficas (OpenSSL), pode degradar a performance da aplicação hospedeira sob carga pesada.
[PT-BR] Mitigação: O módulo Filter (C++) serve exatamente para isso: realizar o descarte rápido de ruído. Apenas eventos anômalos que passaram por esse filtro de pré-classificação ultrarrápido são enviados para a análise pesada da IA (Mojo), mantendo o overhead geral próximo de zero.
3. "False Positive" Risk (Business Disruption) | Risco de "Falso Positivo" (O Bloqueador de Negócio)
[EN] Risk: If the behavioral AI engine (Brain/Mojo) mistakenly flags a legitimate massive system update or an unexpected business sales traffic spike as an active zero-day exploit, it could prematurely terminate or isolate critical infrastructure services.
[EN] Mitigation: The lifecycle enforces a non-blocking "Observation Mode" (passive monitoring) before moving into active enforcement. Furthermore, the core manifest implements strict "Fail-Safe" logic boundaries where, if the AI's classification confidence falls below a safe threshold, the engine defaults to a standard fallback behavior to guarantee business availability over blind termination.
[PT-BR] Risco: Se o motor de IA (Brain/Mojo) classificar uma atualização legítima do sistema ou um pico de tráfego de vendas como uma "ameaça", ele pode derrubar ou isolar serviços críticos da distribuidora.
[PT-BR] Mitigação: O sistema opera em um "Modo de Observação" (monitoramento passivo) antes de ativar o bloqueio definitivo. Além disso, o manifesto de arquitetura prevê mecanismos de "Fail-Safe" onde, em caso de dúvida ou erro da IA, o sistema retorna ao comportamento padrão seguro para não interromper a operação, priorizando a disponibilidade do negócio.
4. The "Double-Edged Sword" (Agent Evasion) | A "Faca de Dois Gumes" (Evasão do Agente)
[EN] Risk: If an advanced persistent threat (APT) discovers the presence of Amphi on a targeted node, they might attempt to target the user-space agent directly, killing the process or manipulating the host systemd architecture to blind the security layout.
[EN] Mitigation: This vulnerability is neutralized by the system's low-level Watchdog architecture. Operating under a rigorous Zero-Trust "Fail-Closed" philosophy, if the user-space agent is terminated or altered without valid cryptographic authorization, the kernel-space hooks immediately lock down network interfaces and isolate the node, containing the threat.
[PT-BR] Risco: Se um atacante descobrir o Amphi, ele pode tentar desativar o agente de segurança especificamente, atacando o processo em user-space ou manipulando o systemd.
[PT-BR] Mitigação: A implementação de um Watchdog de baixo nível que monitora o agente resolve esse risco. Caso o Amphi seja encerrado de forma anômala, o kernel aciona instantaneamente um estado de "Fail-Closed" (travamento preventivo da rede), transformando o sistema de segurança em um componente de confiança zero que não pode ser evadido.
5. Maintenance Complexity (Technical Debt) | Complexidade de Manutenção (Dívida Técnica)
[EN] Risk: Amphi deploys a polyglot architectural footprint (Rust, Go, Mojo, C++, C, TypeScript, Python). This multi-language baseline can introduce steep engineering barriers and technical debt for organization teams maintaining the ecosystem long-term.
[EN] Mitigation: The software is decoupled into strict, independent modules behaving as standalone architectural "organs" with explicit interface contracts. Supported by deep documentation, "scar logs," and clear roadmaps, any systems engineer can fully maintain or patch localized modules without requiring end-to-end knowledge of the overall multi-language stack.
[PT-BR] Risco: O uso de múltiplas linguagens (Rust, Go, Mojo, C++, C, TypeScript, Python) pode se tornar um desafio de manutenção de longo prazo e gerar dívida técnica para uma empresa caso os desenvolvedores originais saiam.
[PT-BR] Mitigação: O projeto é estritamente modularizado em "órgãos" independentes com contratos de comunicação bem definidos. Aliado a isso, o repositório mantém documentações técnicas robustas, logs de cicatrizes (histórico de decisões) e roadmaps detalhados, permitindo que engenheiros mantenham módulos específicos sem a necessidade de dominar todo o ecossistema poliglota.
⚡ Modo Retaliation (Retaliation Mode) | Contra-Ataque Assimétrico
⚠️ [EN] Warning: This mode shifts Amphi from a passive shield to an active evolutionary predator. It does not strike outward to destroy external infrastructure; it turns our internal network into a computational black hole that deconstructs, confuses, and exhausts the adversary within our own boundaries.

⚠️ [PT-BR] Aviso: Este modo muda o Amphi de um escudo passivo para um predador evolucionário ativo. Ele não ataca para fora tentando destruir a infraestrutura externa; ele transforma a nossa própria rede interna em um buraco negro computacional que desconstrói, confunde e exaure o adversário dentro das nossas próprias fronteiras.

🧠 The Strategy | A Estratégia
[EN] Traditional firewalls block malicious connections, letting attackers instantly retry using different vectors. The Retaliation Mode exploits the attacker’s most valuable assets: Time and Compute Power. By utilizing the interconnected capabilities of eBPF, C++, Mojo, and Go, Amphi tricks automated malware into burning its own resources, rendering the economic cost of the cyber-attack unsustainable for the hacker.

[PT-BR] Firewalls tradicionais bloqueiam conexões maliciosas, permitindo que os atacantes tentem instantaneamente novos vetores. O Modo Retaliation explora os recursos mais valiosos do atacante: Tempo e Poder Computacional. Ao utilizar as capacidades interconectadas de eBPF, C++, Mojo e Go, o Amphi força o malware automatizado a queimar seus próprios recursos, tornando o custo financeiro do ataque cibernético insustentável para o hacker.

🛠️ Core Offensive Mechanisms | Mecanismos Ofensivos Centrais
1. Asymmetric Tarpitting | Estrangulamento de Conexão Assimétrico
[EN] Orchestrated by Ghost (Go/Envoy) and Filter (C++). Instead of dropping packets from an active network scanner or brute-force bot, Amphi accepts the connection but streams responses back byte-by-byte at the absolute minimum speed allowed by the TCP/IP window. The attacker's tools remain open, hanging and consuming their local hardware sockets and memory RAM for weeks.
[PT-BR] Orquestrado pelo Ghost (Go/Envoy) e Filter (C++). Em vez de derrubar pacotes de um scanner de rede ativo ou bot de força bruta, o Amphi aceita a conexão, mas envia as respostas de byte em byte na velocidade mínima absoluta permitida pela janela do protocolo TCP/IP. As ferramentas do atacante ficam travadas, consumindo seus sockets de hardware locais e memória RAM por semanas.
2. Command & Control (C2) Poisoning | Envenenamento de Servidores C2
[EN] Executed by Nerves (C/eBPF) and Brain (Mojo). When internal malware attempts to exfiltrate database records to an external C2 server, eBPF intercepts the socket payload. Mojo dynamically generates realistic, high-entropy but completely synthetic and toxic fake data (invalid password hashes, corrupt tokens). The attacker believes the theft was successful, but their remote database is permanently corrupted with garbage.
[PT-BR] Executado pelo Nerves (C/eBPF) e Brain (Mojo). Quando um malware interno tenta exfiltrar registros do banco de dados para um servidor C2 externo, o eBPF intercepta o payload do socket. O Mojo gera dinamicamente dados falsos realistas e de alta entropia, mas totalmente sintéticos e tóxicos (hashes inválidos, tokens corrompidos). O atacante acredita que o roubo funcionou, mas seu banco de dados remoto é corrompido permanentemente com lixo digital.
3. Dynamic Honeypot Shifting | Rotação Dinâmica para Sandbox
[EN] Driven by the Enforcer (Rust). If an intruder gains interactive shell access via a zero-day exploit, the Rust subsystem forks the active container memory. The legitimate business application is silently migrated to a clean namespace, while the attacker's session is isolated inside a restricted sandbox filled with fake environment variables and fabricated system files, letting them attack ghosts.
[PT-BR] Movido pelo Enforcer (Rust). Se um intruso ganha acesso a uma shell interativa através de um exploit zero-day, o subsistema em Rust faz um fork da memória do contêiner ativo. A aplicação legítima do negócio é migrada silenciosamente para um namespace limpo, enquanto a sessão do atacante fica isolada em uma sandbox restrita, cheia de variáveis de ambiente falsas e arquivos de sistema forjados, deixando-o atacando fantasmas.
⚖️ The Line: Inbound Defense vs. Illegal Hack-Back | A Linha Vermelha Ética
[EN] Rule Absolute: Amphi operates strictly under Inbound Defenses. It never executes remote denial-of-service (DDoS) attacks or attempts to breach foreign infrastructure. Since advanced threats route traffic through compromised innocent nodes (hospitals, universities, small businesses), external retaliation is reckless, illegal, and counter-productive. Amphi's warfare is psychological and computational containment within its own infrastructure boundaries.
[PT-BR] Regra Absoluta: O Amphi opera estritamente sob Defesa Inbound. Ele nunca executa ataques de negação de serviço (DDoS) remotos ou tenta invadir infraestruturas externas. Como ameaças avançadas roteiam tráfego através de nós inocentes sequestrados (hospitais, universidades, pequenas empresas), a retaliação externa é irresponsável, ilegal e contra-producente. A guerra do Amphi é de contenção psicológica e computacional estritamente dentro dos limites da sua própria infraestrutura.
📜 Manifesto de Engenharia
[EN] Amphi is not an add-on; it is the environment. We are shifting the security paradigm from "Blocking the Door" to "Building a Living System." In an era of AI-driven cyber-attacks, static defenses are obsolete. We are building the future where infrastructure is self-aware, self-healing, and fundamentally resilient.

[PT-BR] O Amphi não é um adicional; é o meio-ambiente. Estamos mudando o paradigma de segurança de "Trancar a Porta" para "Construir um Sistema Vivo". Em uma era de ataques cibernéticos baseados em IA, defesas estáticas são obsoletas. Estamos construindo o futuro onde a infraestrutura é autoconsciente, capaz de se curar e fundamentalmente resiliente.

⚖️ Licença Copyright (c) 2026 The Amphi Project. All rights reserved.

🤝 Como Contribuir
O Amphi é uma iniciativa massiva de engenharia. Precisamos de especialistas em Segurança de SO, Engenheiros de Dados e Pesquisadores de IA.

Faça um Fork do repositório
Crie uma branch para sua feature (git checkout -b feature/NovaDefesa)
Commit suas mudanças (git commit -m 'Add: Novo hook eBPF para isolamento de rede')
Faça o Push para a branch (git push origin feature/NovaDefesa)
Abra um Pull Request
💻 Configuração Estratégica (amphi.yaml)
O sistema define sua "política de imunidade" de forma declarativa:

version: "2.0-swarm"
amphi:
  # Configuração de defesa coletiva
  cluster:
    federation_mode: "active" # Sincronização em tempo real de padrões de ataque
    auto_heal: true           # Auto-correção de processos críticos

  # Camada de Decepção (MTD)
  deception:
    enable: true
    honey_ports: [22, 3306, 8080] # Portas falsas para induzir o atacante ao erro
    trap_behavior: "deceive"       # O sistema fornece dados falsos ao atacante

  # hardening de runtime
  system_hardening:
    runtime_security:
      - name: "Container-Sandbox"
        target: ["node", "python", "java"]
        deny_syscalls: ["ptrace", "kexec_load"] # Bloqueia técnicas de evasão comuns
        action: "isolate_and_clone"            # Clona a memória para Forensics antes de matar
🛡️ Integração: Amphi + MorphBPF (Hardware-Agnostic Defense)
🇧🇷 Português (PT-BR) | 🇺🇸 English (EN-US)

🇧🇷 Português (PT-BR)
O Amphi agora incorpora o motor MorphBPF, elevando a arquitetura de segurança de rede de "estática" para "adaptável". Esta integração elimina o maior gargalo de soluções de defesa em kernel: a fragmentação de hardware.

🎯 Por que esta integração é crítica?
Soluções tradicionais baseadas em eBPF/XDP frequentemente falham ou sofrem degradação de performance ao serem movidas entre diferentes fabricantes de hardware (Intel, Mellanox, Broadcom), devido às variações nos layouts de memória (offsets) dos drivers. Com o MorphBPF, o Amphi resolve isso de forma autônoma:

Portabilidade Absoluta: O Amphi "escreve uma vez, executa em qualquer lugar". O mesmo binário de segurança é aplicado a qualquer NIC de rede sem a necessidade de recompilação.
Performance de Silício: Ao realizar o patching de bytecode eBPF em tempo real, garantimos que nossas regras de inspeção (L7/L4) interajam diretamente com os buffers de hardware, mantendo a latência quase nula característica do Amphi.
Imunidade a Atualizações de Firmware: Se uma atualização de driver alterar estruturas internas da placa, o motor MorphBPF detecta o deslocamento através do BTF (BPF Type Format) e recalibra a proteção instantaneamente.
⚙️ Como funciona a simbiose
Introspecção de Kernel: O Amphi consulta o sistema para identificar a topologia da NIC e o módulo de driver carregado.
Patching Dinâmico: O motor MorphBPF intercepta o bytecode do Amphi e traduz dinamicamente os endereços de memória, garantindo que os dados (como packet_length, vlan_tag, checksum) sejam lidos corretamente independente da arquitetura.
Execução Segura: O código ajustado passa pelo verificador do kernel e é anexado ao hot-path (XDP/TC) com a máxima eficiência possível.
🇺🇸 English (EN-US)
Amphi now integrates the MorphBPF engine, evolving our network security architecture from "static" to "adaptive." This integration eliminates the biggest bottleneck in kernel-level defense solutions: hardware fragmentation.

🎯 Why this integration is critical?
Traditional eBPF/XDP-based solutions often fail or suffer performance degradation when migrated across different hardware vendors (Intel, Mellanox, Broadcom) due to variations in memory layouts (offsets) within drivers. With MorphBPF, Amphi solves this autonomously:

Absolute Portability: Amphi follows the "Write Once, Run Everywhere" paradigm. The same security binary is applied to any NIC without the need for recompilation.
Silicon-Level Performance: By patching eBPF bytecode at runtime, we ensure that our inspection rules (L7/L4) interact directly with hardware buffers, maintaining the near-zero latency that defines Amphi.
Firmware Update Immunity: Should a vendor firmware update alter internal structure offsets, the MorphBPF engine detects the shift via BTF (BPF Type Format) and recalibrates the defense layer instantly.
⚙️ How the symbiosis works
Kernel Introspection: Amphi queries the system to identify the NIC topology and the loaded driver module.
Dynamic Patching: The MorphBPF engine intercepts Amphi's bytecode and dynamically translates memory addresses, ensuring that data (e.g., packet_length, vlan_tag, checksum) is read correctly, regardless of the architecture.
Secure Execution: The adjusted bytecode passes the kernel verifier and is attached to the hot-path (XDP/TC) with maximum possible efficiency.
🛠️ Configuração de Implementação / Implementation Setup
Adicione a sub-árvore do MorphBPF ao seu diretório src/ e integre via Makefile:

amphi/
├── src/
│   ├── morph-bpf/          # MorphBPF Engine (Rust/C)
│   ├── security-core/      # Amphi Logic (C/eBPF)
│   └── orchestrator/       # Control Plane (Go)
├── Makefile                # Unified build including morphing steps
└── README.md               # This manifesto



Cerberus-Core — Amphi Ecosystem
🇧🇷 Português (PT-BR)
📌 O Significado do Nome: O Guardião do Kernel
Na mitologia grega, Cérbero (Cerberus) é o monstruoso cão de três cabeças que guarda os portões do submundo, garantindo que ninguém entre sem permissão e ninguém escape.

No ecossistema Amphi, o Cerberus-Core assume exatamente essa função. Ele atua como o cão de guarda supremo e inabalável do Kernel do Sistema Operacional. Suas três cabeças representam as três dimensões analíticas que ele monitora simultaneamente, criando uma "prisão triangular" para qualquer ameaça:

Primeira Cabeça (Rede/Lógica): Vigia o estado e o contexto dos fluxos de dados.
Segunda Cabeça (CPU/Física): Vigia o comportamento e o estresse do hardware em nível de silício.
Terceira Cabeça (Memória/Imunidade): Vigia a integridade interna para garantir que a própria defesa nunca seja corrompida.
⚙️ Arquitetura Interna: Como as Três Cabeças Funcionam
O Cerberus-Core não é apenas um filtro; é um organismo autônomo. Ele opera cruzando telemetria de três submódulos críticos que vivem entre o kernel-space e o user-space:

1. flow_state (Rastreamento de Estado - A Rede): O eBPF tradicional é stateless (analisa pacotes isolados). O Cerberus resolve isso injetando mapas de alta performance (Shared Maps). Cada conexão ganha um ciclo de vida persistente, permitindo que o Amphi identifique ataques fracionados em milhares de pacotes e exfiltrações "low-and-slow".
2. hardware_pmu (Inspeção de Canal Lateral - A CPU): Malwares modernos ofuscam código para burlar assinaturas. O Cerberus ignora a assinatura e foca na física. Através dos PMCs (Performance Monitoring Counters), ele lê diretamente do processador. Se um payload ofuscado tentar se descompactar, ele gerará picos absurdos de Cache-Misses e Branch Mispredictions. A anomalia é pega antes da execução.
3. self_guard (Sentinela de Memória - A Autodefesa): Se o invasor tentar atacar a própria engine (via injeção de heap ou buffer overflow), o Cerberus se defende. Ele utiliza Guard Pages e validação criptográfica (HMAC) ao redor de suas tabelas e ponteiros. Qualquer escrita não autorizada resulta em bloqueio instantâneo do atacante.
💻 A Interface de Comando: O cb CLI
Para gerenciar essa complexidade de nível de kernel, o Cerberus utiliza um protocolo de comandos DevOps de alta eficiência acionado pelo prefixo cb.

Os comandos não são meros scripts; eles são gatilhos que atualizam os mapas eBPF e se comunicam assincronamente com o Orquestrador através de sockets:

cb run: Inicia a engine. Executa a validação de privilégios (root), checa a assinatura dos binários, carrega as regras via MorphBPF para contornar problemas de hardware (NIC offsets) e acorda as três cabeças simultaneamente.
cb status: Consulta os anéis de buffer (Ring Buffers) do kernel e devolve telemetria limpa e imediata (conexões rastreadas, estresse de CPU, integridade de memória).
cb watch: Abre uma visão em tempo real focada na identificação de anomalias (similar ao htop, mas voltado para caça de ameaças ativas).
cb freeze <PID>: Comando de reflexo e contenção profunda. Não mata o processo (o que destruiria provas em memória), mas usa Cgroups v2 para limitar a CPU do atacante a 1%, "congelando-o" para análise forense.
🕸️ Integração com o Amphi Inteiro
Entrada (MorphBPF): Ajusta os pacotes independentemente de qual placa de rede (Intel, Mellanox) o servidor usa e os envia limpos ao flow_state.
Correlação (cerberus_orchestrator): Avalia os dados em nanossegundos. Se a Rede for anômala E a CPU der picos de erros físicos = Ataque Confirmado.
Decisão Neural (Brain/Mojo): Toda essa telemetria física e lógica alimenta os tensores do motor em Mojo. O Amphi usa isso para treinar sua Inteligência de Enxame via Aprendizado por Reforço Inverso (IRL), distribuindo a "vacina" para toda a rede antes que o ataque se repita.
Linguagens Dominantes: Rust (80%) para segurança de memória nativa e orquestração assíncrona; C++ (20%) para acesso direto e de zero-latência às APIs de monitoramento físico do Linux (perf_event_open).

🇺🇸 English (EN-US)
📌 The Meaning of the Name: The Kernel Guardian
In Greek mythology, Cerberus is the monstrous three-headed hound that guards the gates of the underworld, ensuring no one enters without permission and no one escapes.

Within the Amphi ecosystem, Cerberus-Core serves exactly this purpose. It acts as the ultimate, unyielding watchdog of the Operating System Kernel. Its three heads represent the three analytical dimensions it continuously monitors, establishing a "triangular prison" for any threat:

First Head (Network/Logic): Watches the state and context of data flows.
Second Head (CPU/Physics): Watches the behavior and stress of hardware at the silicon level.
Third Head (Memory/Immunity): Watches internal integrity to ensure the defense itself is never compromised.
⚙️ Internal Architecture: How the Three Heads Work
Cerberus-Core isn't just a filter; it's an autonomous organism. It operates by cross-referencing telemetry from three critical submodules residing between kernel-space and user-space:

1. flow_state (Stateful Tracking - The Network): Traditional eBPF is stateless. Cerberus overcomes this by injecting high-performance memory structures (Shared Maps). Every connection is given a persistent lifecycle, allowing Amphi to piece together fragmented exploits and detect "low-and-slow" exfiltration attempts.
2. hardware_pmu (Side-Channel Inspection - The CPU): Modern malware obfuscates code to evade signatures. Cerberus ignores the signature and focuses on physics. By reading the PMCs (Performance Monitoring Counters) directly from the processor, it detects when an obfuscated payload attempts to unpack itself, causing drastic spikes in Cache-Misses and Branch Mispredictions. The anomaly is caught before execution.
3. self_guard (Memory Sentinel - The Self-Defense): Should an attacker target the engine itself (via heap injection or buffer overflows), Cerberus strikes back. It surrounds its tables and pointers with Guard Pages and runtime cryptographic validation (HMAC). Any unauthorized write attempt instantly locks the attacker out.
💻 The Command Interface: The cb CLI
To manage this kernel-level complexity, Cerberus uses a highly efficient DevOps command protocol triggered by the cb prefix.

These commands are not merely scripts; they are triggers that update eBPF maps and communicate asynchronously with the Orchestrator via UNIX sockets:

cb run: Bootstraps the engine. It validates root privileges, checks binary signatures, loads rules via MorphBPF to bypass hardware layout issues (NIC offsets), and awakens all three heads simultaneously.
cb status: Queries the kernel's Ring Buffers and returns clean, immediate telemetry (tracked connections, CPU stress levels, memory integrity).
cb watch: Opens a real-time monitoring view tailored for anomaly identification (similar to htop, but designed for active threat hunting).
cb freeze <PID>: A deep-containment reflex command. Instead of killing the process (which destroys in-memory evidence), it uses Cgroups v2 to throttle the attacker's CPU usage to 1%, essentially "freezing" them for forensic analysis.
🕸️ Integration with the Entire Amphi Project
Ingestion (MorphBPF): Standardizes packets regardless of the underlying network card (Intel, Mellanox) and passes clean data to the flow_state.
Correlation (cerberus_orchestrator): Evaluates inputs in nanoseconds. If the Network looks anomalous AND the CPU registers physical spikes = Confirmed Attack.
Neural Decision (Brain/Mojo): All physical and logical telemetry feeds into the Mojo-powered tensor engine. Amphi uses this data to train its Swarm Intelligence via Inverse Reinforcement Learning (IRL), instantly distributing the "vaccine" across the network before the attack can spread.
Core Languages: Rust (80%) for compile-time memory safety and async orchestration; C++ (20%) for direct, zero-latency access to Linux's physical monitoring APIs (perf_event_open).

💎 AmphiLang: The Vertical Engine / O Motor Vertical
Verifier-Aware: A linguagem garante matematicamente que o código gerado será aceito pelo Kernel Verifier. Chega de "tentativa e erro" no eBPF.
Stateful Security: Monitoramento de fluxos de rede persistentes, identificando ataques lentos (low-and-slow) que firewalls comuns ignoram.
Performance Absoluta: Compilação direta via MLIR para eBPF Bytecode, unindo abstração de alto nível com a brutalidade do silício.
⚙️ The Dual Nature: Language & Runtime / A Natureza Dual: Linguagem e Runtime
🇧🇷 PT-BR O Amphi funciona através da simbiose entre dois componentes que operam em camadas distintas:

Como Linguagem (AmphiLang): O nível de abstração (Compiler Front-end). Escreve-se lógica em sintaxe declarativa; o compilador MLIR garante que o programa seja livre de bugs de memória.
Como Programa (Cerberus-Core): O Runtime (Execution Engine). Binário em Rust de alta performance que carrega o bytecode, gerencia a IA (Mojo) e orquestra a mitigação.
🇺🇸 EN-US Amphi functions through the symbiosis of two components operating at distinct layers:

As a Language (AmphiLang): The abstraction layer (Compiler Front-end). Logic is written in declarative syntax; the MLIR compiler ensures the program is free of memory bugs.
As a Program (Cerberus-Core): The Runtime (Execution Engine). A high-performance Rust binary that loads the bytecode, manages the AI (Mojo), and orchestrates mitigation.
🧠 Human-in-the-Loop: The Glass Box Philosophy
🇧🇷 PT-BR O Amphi inverte a lógica do mercado: a IA depende do Humano.

Maestro vs. Orquestra: O desenvolvedor dita as políticas via AmphiLang. A IA executa a mitigação.
amphi explain <id>: Traduzimos incidentes em linguagem humana, sugerindo patch de código diretamente na sua IDE.
Security Systems Architect: Transformamos programadores em especialistas que gerenciam a imunidade da empresa.
🇺🇸 EN-US Amphi flips market logic: AI depends on the Human.

Maestro vs. Orchestra: The developer dictates policies via AmphiLang. The AI executes mitigation.
amphi explain <id>: We translate incidents into human language, suggesting code patches directly in your IDE.
Security Systems Architect: We turn programmers into experts who manage company-wide immunity.
💻 Amphi Developer CLI: The Toolchain
# 1. Iniciar projeto
amphi init --name defense-system

# 2. Compilar com verificação matemática via MLIR
amphi build ./rules/firewall.amphi

# 3. Analisar impacto antes do deploy
amphi analyze ./rules/firewall.amphi

# 4. Carregar no Kernel via Cerberus-Core
sudo amphi load ./build/firewall.o

# 5. Modo Mentor: Explicar incidente
amphi explain <incident_id>

# 6. Monitoramento em tempo real
amphi watch --filter "sql-injection"
🇵🇹 Como funciona a Amphi Developer CLI:
A CLI funciona como o "centro de controle" da sua stack de segurança. Ela abstrai a complexidade do kernel através de três pilares:

Compilação e Verificação (O "Cérebro"): Quando você executa amphi build, a CLI aciona o compilador baseado em MLIR. Ele transforma seu código de alto nível (AmphiLang) em eBPF Bytecode altamente otimizado. Durante esse processo, ele realiza uma checagem matemática que garante que seu código nunca será rejeitado pelo Kernel Verifier.

Gestão de Estado e Deploy (O "Braço"): O comando amphi load não apenas injeta código; ele gerencia a integração contínua do seu Cerberus-Core. Ele assegura que o novo bytecode seja inserido com segurança, sem a necessidade de reiniciar o sistema, mantendo a imunidade do enxame constante.

Telemetria Educacional (O "Mentor"): Com amphi explain, a CLI atua como um tradutor. Ela cruza os logs brutos e o estado de memória (snapshot) capturados pelo Cerberus com a inteligência do Mojo Brain, entregando para você o motivo de um ataque ter sido bloqueado, em uma linguagem que qualquer desenvolvedor entende.

🇺🇸 How the Amphi Developer CLI works?
The CLI operates as the "control center" for your security stack. It abstracts kernel complexity through three pillars:

Compilation and Verification (The "Brain"): When you run amphi build, the CLI triggers the MLIR-based compiler. It transforms your high-level code (AmphiLang) into highly optimized eBPF Bytecode. During this process, it performs a mathematical check that guarantees your code will never be rejected by the Kernel Verifier.

State Management and Deployment (The "Arm"): The amphi load command does not just inject code; it manages the continuous integration of your Cerberus-Core. It ensures that new bytecode is inserted safely without needing a system reboot, keeping the swarm's immunity constant.

Educational Telemetry (The "Mentor"): With amphi explain, the CLI acts as a translator. It correlates raw logs and memory states (snapshots) captured by the Cerberus with the Mojo Brain’s intelligence, delivering the reason an attack was blocked in a language any developer can understand.
