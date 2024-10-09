# gazebo-to-ros2

Este pacote tem como objetivo criar uma cena simples no Gazebo com um LiDAR dentro de um galpão. Além disso, ele inicializa o `gzbridge` que faz a conexão entre os tópicos do Gazebo e do ROS 2.

## Pré-requisitos

- **ROS 2** (Foxy, Galactic, Humble ou posterior)
- **Gazebo** compatível com a versão do ROS 2 instalada
- Pacotes do **gazebo_ros_pkgs**
- **gzbridge** instalado e configurado

## Clonando o Repositório
Para clonar este repositorio:

```bash
git clone https://github.com/PPGIA-Sistemas-Ciberfisicos/gazebo-to-ros2.git
```

## Construindo o Pacote

Após clonar o repositório, navegue até o diretório do pacote e construa-o usando o colcon:

```bash
cd gazebo-to-ros2
colcon build
```

Não se esqueça de source o ambiente após a construção:

```bash
source install/setup.bash
```

## Executando o Launch

Para iniciar a cena no Gazebo e inicializar o `gzbridge`, execute:

```bash
ros2 launch gazebo_to_ros2 gazebo_launch.py
```

Este comando irá:

- Carregar a cena com o LiDAR dentro do galpão no Gazebo.
- Inicializar o `gzbridge` para conectar os tópicos do Gazebo com o ROS 2.

## Verificando os Tópicos

Para listar os tópicos disponíveis:

```bash
ros2 topic list
```

Isso permitirá visualizar os tópicos que estão sendo publicados e subscritos, tanto pelo Gazebo quanto pelo ROS 2.