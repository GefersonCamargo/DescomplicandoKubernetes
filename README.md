# DescomplicandoKubernetes
## Estudos Kubernetes

O Kubernetes, também conhecido como K8S, é uma plataforma de código aberto para automatizar a implantação, o dimensionamento e a gestão de aplicações em contêineres. É uma ferramenta amplamente utilizada no desenvolvimento de sistemas distribuídos e na orquestração de contêineres.

Ao estudar o K8S, é importante entender os conceitos fundamentais, como pods, serviços, implantações e ingressos. Além disso, também é necessário aprender a usar ferramentas como o kubectl para interagir com um cluster Kubernetes e gerenciar os recursos.

Existem diversas fontes de estudo disponíveis, como documentação oficial, tutoriais online, cursos e livros. É recomendado começar com uma introdução aos conceitos básicos e, em seguida, aprofundar-se em áreas específicas, como escalabilidade, monitoramento e segurança.

Os estudos de K8S podem ser desafiadores, mas são extremamente valiosos para profissionais de desenvolvimento e operações que desejam trabalhar com sistemas modernos e escaláveis.

---

![image](https://github.com/GefersonCamargo/DescomplicandoKubernetes/assets/40033929/a95abad5-e653-441a-b30e-af46e96e0fd0)


# CONTROL PLANE

O Control Plane do Kubernetes é composto por três componentes principais: ETCD, Kube APIServer e Kube Scheduler.

### ETCD

A função do ETCD é atuar como o banco de dados do cluster Kubernetes, responsável por armazenar chave/valor e guardar todo o estado real do cluster. Ele guarda as informações do Kube APIServer, que é o único componente que se comunica com o ETCD.

### Kube APIServer

O Kube APIServer é um componente responsável por toda a comunicação do cluster Kubernetes. Ele é responsável por comunicar o status e centralizar as informações de todo o cluster. Além de realizar essa parte de comunicação, ele também é responsável por armazenar as informações dentro do nosso ETCD, que atua como o banco de dados do cluster Kubernetes.

### Kube Scheduler

O Kube Scheduler é um componente responsável por tomar decisões de alocação de recursos e agendar os pods em nós disponíveis dentro do cluster. Ele considera fatores como requisitos de recursos dos pods, políticas de afinidade e anti-afinidade, restrições de recursos e prioridades para realizar o agendamento de forma eficiente e otimizada.

### Kube Controller Manager

O Kube Controller Manager é um componente do Control Plane do Kubernetes responsável por garantir o funcionamento adequado do cluster. Ele é composto por vários controladores que monitoram o estado do cluster e tomam ações para mantê-lo consistente.

Alguns exemplos de controladores incluem o controlador de replicação, que garante que o número desejado de réplicas de um pod seja mantido em execução, e o controlador de serviço, que garante que os serviços estejam corretamente configurados e roteados para os pods correspondentes.

O Kube Controller Manager é essencial para a operação confiável e estável de um cluster Kubernetes, garantindo a consistência e o bom funcionamento dos recursos do cluster.

# WORKERS

### Kubelet

O Kubelet é um agente que roda em cada nó do cluster e é responsável por garantir que os containers sejam executados corretamente. Ele recebe instruções do Kube APIServer sobre os pods que devem ser executados no nó e realiza as ações necessárias para iniciar, parar ou reiniciar os containers conforme necessário. O Kubelet também monitora o estado dos pods e relata quaisquer problemas ao Kube APIServer.

O Kubelet desempenha um papel crucial no funcionamento e na integridade de um cluster Kubernetes, garantindo que os pods sejam executados de forma precisa e eficiente nos nós do cluster.

### Kube Proxy

O Kube Proxy é um componente responsável por gerenciar o acesso de rede aos serviços dentro do cluster Kubernetes. Ele é executado em cada nó do cluster e configura as regras de redirecionamento de tráfego para os pods correspondentes aos serviços.

O Kube Proxy é responsável por implementar o balanceamento de carga entre os pods de um serviço, garantindo que as solicitações de rede sejam distribuídas de forma equilibrada. Ele também lida com a descoberta de serviços no cluster, permitindo que os clientes acessem os serviços pelos seus nomes.

O Kube Proxy desempenha um papel fundamental na conectividade e na comunicação entre os componentes dentro do cluster Kubernetes, garantindo a disponibilidade e o roteamento correto das solicitações de rede.

# Portas TCP/UDP dos componentes do Kubernets

### Kube APIserver ⇒ 6443 TCP

### ETCD ⇒ 2379 - 2380 TCP

### Kube Scheduler ⇒ 10251 TCP

### Kubelet  ⇒ 10250 TCP

### Kube Controller ⇒ 10252 TCP

### Node Port ⇒ 30.000 - 32.767 TCP

### Weave Net ⇒ 6783 - 6784 TCP/UDP


https://www.notion.so/Kubernetes-K8S-d9a8256bd91443378f99b02506024731?pvs=4
