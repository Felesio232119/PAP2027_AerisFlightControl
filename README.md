# Aeris Flight Control
**PAP 2027 – TGPSI, Escola Secundária de Vergílio Ferreira**
Aluno: Leonardo O. S. Ferreira · Turma 12.º 13.ª · N.º 14
Professor orientador: Jorge Silva

## Descrição
O Aeris Flight Control será um sistema de controlo de um drone, em ambiente simulado, que permite testar as funcionalidades sem riscos ou custos. Ele terá como principal objetivo fazer com que um drone descole e aterre, e faça um percurso, tudo através de um controlador PID. E os objetivos mais ambiciosos do projeto serão permitir que o drone desvie de obstáculos pré-definidos, tenha fatores como vento e bateria em conta durante a simulação, e adaptar o código em Python para C++, de maneira que o controlador possa ser aplicado num ESP32. Em conjunto com os scripts de controlo, será feita uma interface em Python, para exibir as informações de voo do drone. Os dados de cada voo, como altitude e velocidade, serão guardados numa base de dados MySQL, oque permite consultá-los na interface e comparar os dados entre voos.

## Objetivos
- Desenvolver em Python um controlador PID que estabilize um drone simulado e mantenha a altitude.
- Fazer o drone cumprir uma missão de forma autónoma: descolar, seguir pontos de passagem e aterrar.
- Guardar os dados de cada voo numa base de dados MySQL e apresentá-los numa interface com gráficos.

## Funcionalidades
### Núcleo mínimo (obrigatório)
- [ ] Descolar, estabilizar e manter a altitude com um controlador PID
- [ ] Seguir um percurso definido por pontos de passagem e aterrar
- [ ] Guardar os dados de cada voo (altitude, velocidade) numa base de dados MySQL
- [ ] Interface em Python com gráficos de altitude, velocidade e resposta do PID

### Extras (se houver tempo)
- [ ] Desviar de uma zona proibida (primeiro com o mapa conhecido, depois com sensores de distância simulados)
- [ ] Incluir vento e bateria na simulação
- [ ] Comparar voos guardados para ajustar os parâmetros do PID
- [ ] Adaptar o controlador de Python para C++ e executá-lo num ESP32 (com sensor MPU6050)

## Tecnologias
| Camada | Tecnologia |
| --- | --- |
| Interface | Python, Matplotlib (biblioteca de janelas a decidir, por exemplo CustomTkinter) |
| Simulação e controlo (em vez de servidor) | Python, PyBullet, gym-pybullet-drones, NumPy |
| Base de dados | MySQL |
| Outras | Git e GitHub, VS Code; C++ e ESP32 (extensão, se houver tempo) |

## Base de dados (tabelas previstas)
- voos (identificador, data, nível de dificuldade, parâmetros do PID)
- leituras (identificador, voo a que pertence, instante, posição, altitude, velocidade, bateria)

A estrutura final será definida na fase de modelação (novembro).

## Planeamento
| Fase | Período | Estado |
| --- | --- | --- |
| Análise e modelação da base de dados, instalação do simulador | nov | Por fazer |
| Desenvolvimento do núcleo mínimo (PID, percurso, aterragem, base de dados e interface) | dez – mar | Por fazer |
| Testes, correções e objetivos extras | abr – mai | Por fazer |
| Relatório e apresentação | mai – jun | Por fazer |

## Registo de progresso
- 26/10/2026 – Proposta de anteprojeto redigida.
- [data] – Criação do repositório e apresentação do projeto.
