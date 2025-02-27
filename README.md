# GitHand - Controle de comandos Git por gestos das mãos :raised_hand_with_fingers_splayed:	
## Motivação do projeto :thought_balloon: :
Enquanto estava escrevendo códigos, no momento em que eu precisava usar comandos específicos da ferramenta Git, eu esquecia de alguns detalhes deles(como uma palavra ou um caractere específico) e isso gerava erros que atrapalhavam a minha linha de raciocínio que eu estava desenvolvendo para escrever o código, e me atrasavam.  

Portanto, visando praticidade, pensei em uma solução que usasse visão computacional para que, a partir de simples gestos(intuitivos e mais fáceis de se lembrar do que linhas de códigos com vários caracteres específicos), eu pudesse dinamizar os comandos Git.

## Bibliotecas e lógicas utilizadas :open_book:	:
### -OpenCv 👀: Captação de frames da câmera, bem como escrita sobre esses frames de qual gesto está sendo exibido

### -MediaPipe 🙌: Uso dos frames captados pelo OpenCv para desenhar landmarks das mãos juntamente com pontos, cujas coordenadas foram fundamentais para o preparo do DataSet

### -CSV 🗃️: Usada para escrever o rótulo(nome do gesto da mão) como dado de saída, e as posições dos pontos nas landmarks da mão como dados de entrada no arquivo csv(usado para o Machine Learning)

### -Pandas 🐼: Usada para abrir o arquivo CSV onde estão os dados e coletá-los de modo organizado para o aprendizado de máquina

### -SciKit-Learn 🤖: Dela, usei o algoritmo de aprendizado supervisionado de máquina Random Forest 🌳, altamente eficiente, garantindo uma acurácia de 94%

### -Joblib 📚: Salva/Armazena o modelo de I.A treinado para ser usado em outros arquivos de modo instantâneo

### -Tkinter :computer:	: Criação de interface gráfica simples para o usuário interagir e colocar informações , como o link do respositório do GitHub 

### -Pillow :framed_picture: : Usada para colocar a imagem de fundo e estilizar a janela do Tkinter

### -Subprocess :keyboard: : Usada para escrever os comandos Git no terminal da IDE (no caso Visual Studio Code) correspondentes aos gestos de mão 

### -Numpy :1234:	: Usada para converter os Data Features em array para assim o modelo de máquina conseguir fazer uma previsão de qual gesto a mão está fazendo, dado a posição dos pontos nos landmarks

### -Time ⏲️ : Usada para gerar delay de cerca de 5 segundos quando algum gesto é reconhecido, a fim de evitar travamentos na execução do código

## Gestos reconhecidos até então 🤙 : 
### Primeiro :point_up: : Sinaliza o início de um repositório no GitHub
### Positivo 👍: Sinaliza a permissão de submissão de um commit
### "VoltaMain" :point_left: : Sinaliza a volta para o branch main
### "V" :v:	: Sinaliza a criação de um branch juntamente com um commit
### Ok(Trocar) 👌 : Sinaliza a permissão de acesso/troca para algum outro branch existente 

### Exemplo do que pode ser evitado/simplificado pelo projeto:

![Captura de tela 2025-02-27 113256](https://github.com/user-attachments/assets/e88dda29-db01-43aa-b732-b2edda581484)

Tudo isso pode ser feito apenas levantando o dedo indicador(Gesto primeiro)

### P.S ⚠️ : Ainda há pequenas imprecisões na determinação de gestos, mas isso pode ser facilmente melhorado ao fornecer mais imagens ao treinamento da I.A

## Print 📸 -  Funcionamento do GitHand :

![Captura de tela 2025-02-27 095607](https://github.com/user-attachments/assets/f4621186-51d2-4771-9755-b89d7f8c2c29)
