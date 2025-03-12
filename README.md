Tipos de Nuvem
1.	Nuvem Privada
o	Infraestrutura exclusiva para uma organização, oferecendo maior controle sobre segurança e dados.
o	A empresa é responsável pela manutenção, atualizações e escalabilidade dos recursos.
2.	Nuvem Pública
o	Recursos fornecidos por terceiros, acessíveis pela internet, reduzindo custos iniciais.
o	Permite escalabilidade rápida, com pagamento apenas pelo uso efetivo dos serviços.
3.	Nuvem Híbrida
o	Combina infraestrutura privada e pública, equilibrando segurança e flexibilidade.
o	Permite distribuição de cargas de trabalho conforme necessidade e regulamentação.
4.	Multi-cloud (Não cai na prova)
o	Uso de múltiplos provedores de nuvem para aumentar resiliência e evitar dependência de um único fornecedor.
Modelos de Custo
1.	CapEx (Despesas de Capital)
o	Investimento inicial em hardware e infraestrutura, amortizado ao longo do tempo.
o	Permite previsão de gastos a longo prazo, mas exige maior capital inicial.
2.	OpEx (Despesas Operacionais)
o	Pagamento pelo consumo de recursos e serviços conforme a necessidade da empresa.
o	Custos flexíveis e previsíveis, sem necessidade de grandes investimentos iniciais.
3.	Modelo Baseado em Consumo
o	Cobrança proporcional ao uso real dos recursos de nuvem, sem desperdício financeiro.
o	Garante melhor previsão de custos e otimização dos investimentos em TI.

Benefícios da Nuvem no Azure
1.	Alta Disponibilidade
o	O Service Level Agreement (SLA) define o nível de disponibilidade esperado para os serviços na nuvem.
o	Um SLA de 99,9% representa até 8,76 horas de indisponibilidade por ano.
o	O Azure Service Health permite monitorar se um serviço está operacional, degradado ou indisponível.
o	Diferentes níveis de disponibilidade, como zonas de disponibilidade e replicação geográfica, garantem maior resiliência.
2.	Escalabilidade e Elasticidade
o	Escalabilidade permite aumentar ou diminuir recursos, como armazenamento e processamento, conforme a necessidade.
o	Elasticidade ajusta automaticamente os recursos para suportar variações na demanda, evitando desperdícios.
o	Exemplo: adicionar máquinas virtuais (VMs) ou contêineres para lidar com picos de uso.
3.	Confiabilidade
o	A infraestrutura descentralizada da nuvem garante alta resiliência e continuidade dos serviços.
o	Recursos são implantados em múltiplas regiões, reduzindo o impacto de falhas localizadas.
o	O modelo distribuído previne falhas catastróficas e assegura recuperação de desastres eficiente.
4.	Previsibilidade
o	Permite prever desempenho e custos, garantindo estabilidade financeira e operacional.
o	O Microsoft Azure Well-Architected Framework ajuda a criar arquiteturas eficientes.
o	O modelo pay-as-you-go ajusta custos ao consumo real, evitando desperdícios.
5.	Segurança
o	O Azure fornece ferramentas avançadas de segurança, como Azure Security Center e Microsoft Defender for Cloud.
o	A responsabilidade da segurança é compartilhada:
	A Microsoft protege a infraestrutura física e os serviços de base.
	O cliente deve configurar firewalls, permissões e políticas de segurança corretamente.
o	Atualizações e patches de segurança precisam ser gerenciados pelo cliente para evitar vulnerabilidades.
6.	Governança
o	A governança na nuvem garante conformidade com normas regulatórias e boas práticas.
o	Ferramentas como Azure Policy e Azure Blueprints permitem auditoria e aplicação de políticas de conformidade.
o	Implementar a governança desde o início ajuda a manter o ambiente seguro e bem gerenciado.
7.	Gerenciabilidade
o	O Azure oferece diversas opções para implantar e gerenciar recursos:
	Portal Web (Azure Portal) – Interface gráfica para administração dos serviços.
	Linha de Comando (Azure CLI) – Para automação e scripts.
	APIs REST – Para integração com outros sistemas.
	PowerShell – Administração avançada e automação de processos.
o	O uso de modelos de implantação evita configurações manuais repetitivas e melhora a eficiência operacional, além de evitar erros.

IaaS PaaS SaaS

IaaS (Infra como seriço)

Crie uma estrutura de TI de pagamento conforme o uso, alugando servidores,
VM, armazenamento, redes e sistemas operacionais de um provedor de
nuvem.

1. Servidores e armazenamento
2. Firewall/segurança de rede
3. Planta física/edifício do datacenter (rede, por exemplo, a uma rede privada)

Serviço de nuvem mais flexível
Você configura e gerência o hardware para seu aplicativo

PaaS (Plataforma como serviço)

Engloba o IaaS e acresce, por exemplo:
1. Sistemas operacionais
2. Ferramentas para desenvolvedores, análise de negócios de
gerenciamento de database.
Fornece um ambiente para a criação, o teste e a implantação de aplicativos
de softwares, sem foca no gerenciamento da infraestrutura subjacente.

Focado no desenvolvimento de aplicativos
O gerenciamento da plataforma é realizado pelo provedor de assiantura

SaaS (Software como serviço)

1. Engloba IaaS, PaaS
2. Aplicativo e apps hospedados

Arquitetura do Azure

1. Regiões do Azure 

O Azure é dividido em regiões, que são locais geográficos ao redor do mundo onde os data centers estão localizados. Cada região contém um ou mais data centers e oferece serviços específicos.
📌 Exemplos de Regiões:
•	Leste dos EUA (East US)
•	Oeste da Europa (West Europe)
•	Sudeste Asiático (Southeast Asia)
•	Brasil Sul (Brazil South)
Cada região é independente, permitindo que os clientes escolham onde hospedar seus serviços com base em latência, conformidade e requisitos operacionais.

2. Zonas de Disponibilidade

Uma região pode ter Zonas de Disponibilidade, que são múltiplos data centers fisicamente separados dentro da mesma região. Cada zona tem:
✅ Energia, rede e refrigeração independentes
✅ Alta disponibilidade para cargas de trabalho críticas
✅ Replicação síncrona de dados entre zonas
📍 Exemplo: Uma aplicação pode ter três máquinas virtuais em três zonas diferentes dentro da mesma região, garantindo continuidade do serviço em caso de falha de um data center.

3. Pares de Regiões

O Azure agrupa regiões em pares, garantindo maior resiliência e recuperação de desastres. Cada região tem um par geograficamente distante, e o Azure prioriza a recuperação primeiro na região emparelhada em caso de falhas catastróficas.
📌 Exemplos de Pares de Regiões:
•	Brasil Sul ↔ Sul dos EUA
•	Norte da Europa ↔ Oeste da Europa
•	Leste do Japão ↔ Oeste do Japão
🛑 Vantagens dos pares de regiões:
✔ Atualizações do Azure são aplicadas primeiro em uma região e depois na outra para evitar downtime
✔ Replicação assíncrona entre regiões para recuperação de desastres
✔ Continuidade dos serviços críticos em caso de falha total de uma região

Grupos de Gerenciamento no Azure 

Os Grupos de Gerenciamento (Management Groups) são um recurso do Azure que permite organizar e gerenciar várias assinaturas de forma centralizada. Eles são úteis para aplicar políticas, controles de acesso e compliance em larga escala.

📌 Estrutura Hierárquica do Azure
A estrutura organizacional do Azure é hierárquica e segue esta ordem:
🔹 Grupos de Gerenciamento (Nível mais alto)
🔹 Assinaturas
🔹 Grupos de Recursos
🔹 Recursos Individuais (VMs, Storage, Banco de Dados, etc.)
Cada Grupo de Gerenciamento pode conter várias assinaturas, que por sua vez contêm grupos de recursos e recursos individuais.


Modelo de preço de pagamento conforme o uso

Os usuários pagam pelo software que utilizam em um modelo de assinatura

Modelo de responsabilidade partilhada

