# Dispositivo de Acessibilidade para Tetraplégicos baseado em Movimento da Cabeça

Este projeto apresenta um dispositivo de acessibilidade desenvolvido para auxiliar pessoas tetraplégicas a utilizarem computadores, celulares e outros dispositivos eletrônicos por meio de movimentos da cabeça.  

O sistema foi desenvolvido como Trabalho de Conclusão de Curso (TCC) e busca oferecer uma solução de baixo custo, adaptável e com potencial de aplicação em larga escala em instituições de reabilitação, escolas e ambientes domésticos.

---

## Objetivo

Permitir que pessoas com severas limitações motoras controlem dispositivos eletrônicos utilizando apenas movimentos da cabeça e pequenos gestos voluntários, promovendo:

- Maior autonomia no uso de tecnologias digitais  
- Inclusão educacional e profissional  
- Melhora na comunicação e interação social  

---

## Visão Geral do Sistema

O dispositivo é composto por:

- **Módulo principal** instalado em um boné/capacete
- **Sensores inerciais** para detecção da inclinação e movimentos da cabeça
- **Microcontrolador com comunicação sem fio** para atuar como mouse/controle
- **Sensores adicionais (como botões ou sensores de pressão)** para cliques e comandos extras

Através do processamento dos dados dos sensores, os movimentos da cabeça são convertidos em comandos como:

- Movimento do cursor na tela  
- Clique esquerdo / direito  
- Rolagem  
- Ações configuráveis (atalhos, confirmação, etc.)

---

## Tecnologias Utilizadas

- **Microcontrolador:** ESP32 (ou similar com Bluetooth/Wi-Fi)
- **Sensor inercial:** MPU6050 ou equivalente (acelerômetro + giroscópio)
- **Comunicação:** Bluetooth (perfil HID / BLE-Mouse) para emular mouse ou ponteiro
- **Linguagem de programação:** C/C++ (Plataforma Arduino/ESP-IDF)
- **Protótipo físico:** Montado em boné/capacete com suporte para os sensores e fiação interna

*(Ajuste os itens acima conforme o seu hardware real.)*

---

## Funcionamento

1. **Captura de movimento**  
   O sensor inercial mede a inclinação e rotação da cabeça nos eixos X, Y e Z.

2. **Processamento dos dados**  
   O microcontrolador aplica filtros e calibração para transformar os dados brutos dos sensores em movimentos suaves e estáveis.

3. **Mapeamento para comandos**  
   - Inclinar a cabeça para frente/trás/direita/esquerda → movimento do cursor na tela  
   - Permanecer parado em determinada posição → cursor estável  
   - Pressionar um sensor/botão ou realizar gesto configurado → clique ou ação específica  

4. **Envio ao dispositivo eletrônico**  
   Via Bluetooth, o ESP32 se comporta como um mouse sem fio, sendo reconhecido por computadores, tablets e celulares compatíveis.

---

## Principais Funcionalidades

- Controle de cursor via movimentos da cabeça  
- Cliques configuráveis (esquerdo, direito, duplo clique)  
- Ajuste de sensibilidade dos movimentos  
- Modo de calibração inicial para cada usuário  
- Uso sem necessidade de drivers específicos (dispositivo reconhecido como mouse Bluetooth)

---

## Público-Alvo

- Pessoas tetraplégicas ou com limitações severas nos membros superiores  
- Pacientes em processo de reabilitação motora  
- Instituições de ensino inclusivo  
- ONGs e centros de apoio a pessoas com deficiência

---

## Metodologia (Resumo para TCC)

1. **Pesquisa e revisão bibliográfica**  
   Estudo de soluções de acessibilidade existentes, interfaces cérebro-computador, dispositivos comerciais e projetos open-source similares.

2. **Definição de requisitos**  
   - Baixo custo  
   - Fácil utilização e adaptação  
   - Compatibilidade com múltiplos dispositivos  
   - Segurança e conforto para o usuário

3. **Desenvolvimento do protótipo**  
   - Seleção e testes de sensores  
   - Programação do firmware no microcontrolador  
   - Construção do suporte físico (boné/capacete)  

4. **Testes com usuários**  
   - Aplicação do protótipo em usuários reais (em parceria com instituição/ONG)  
   - Observação de usabilidade, conforto e curva de aprendizado  
   - Coleta de feedback qualitativo e quantitativo

5. **Ajustes e melhorias**  
   Lapidação da sensibilidade, ergonomia e mapeamento dos comandos conforme a necessidade dos usuários.

---

## Resultados Esperados

- Redução da dependência de terceiros para tarefas simples em computadores/celulares  
- Acesso facilitado a recursos educacionais, de comunicação e entretenimento  
- Prova de conceito de que dispositivos de acessibilidade podem ser produzidos com custo reduzido e tecnologia amplamente disponível

*(Aqui você pode adicionar dados reais: número de usuários que testaram, tempo médio para se adaptar, relato de caso, etc.)*

---

## Como Usar

1. **Ligar o dispositivo**  
   Ative o módulo no capacete/boné (chave liga/desliga ou botão).

2. **Emparelhar com o dispositivo eletrônico**  
   - Ative o Bluetooth do computador/celular  
   - Procure pelo dispositivo (ex.: `HeadMouse_TCC`)  
   - Conclua o emparelhamento

3. **Calibração inicial**  
   - Sente-se em posição confortável, olhando para frente  
   - Ative o modo de calibração (por botão ou comando pré-definido)  
   - Aguarde a confirmação

4. **Operação**  
   - Movimente a cabeça suavemente para direcionar o cursor  
   - Utilize os sensores/botões para cliques e confirmações  

---

## Limitações e Trabalhos Futuros

- Dependência de boa postura e apoio da cabeça  
- Possível fadiga em uso prolongado  
- Necessidade de calibração personalizada para cada usuário  

**Possíveis expansões:**

- Integração com comandos de voz  
- Uso de algoritmos de inteligência artificial para prever intenções e suavizar movimentos  
- Versão com bateria de maior autonomia  
- Integração com sistemas de comunicação alternativa (teclados virtuais, interfaces de comunicação para PCD)

---

## Autoria

Este projeto foi desenvolvido por **[Seu Nome]** como requisito parcial para conclusão do curso **[Nome do Curso / Instituição]**.

Orientador(a): **[Nome do orientador]**

---

## Licença

Definir licença conforme objetivo do projeto:

- Uso acadêmico apenas  
- Ou licença open-source (ex.: MIT, GPL, etc.)

