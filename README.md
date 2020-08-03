# Casos de Uso

O RPA para a API simples e poderosa do Python torna a automação de processos robóticos divertida! Você pode usá-lo para automatizar rapidamente tarefas repetitivas e demoradas, independentemente de as tarefas envolverem sites, aplicativos de desktop ou a linha de comando.


# Referência da API
Confira o exemplo de script Python , a solução RPA Challenge e o exemplo do RedMart mantimentos . Para automatizar o navegador Chrome invisivelmente, veja este simples truque . Para executar 20 a 30 vezes mais rápido, sem atrasos normais na interação da interface do usuário, consulte este hack avançado .

##IDENTIFICADORES DE ELEMENTOS
Um identificador de elemento ajuda a informar ao RPA para Python exatamente com qual elemento na interface do usuário você deseja interagir. Por exemplo, // * [@ id = "email"] é um XPath apontando para o elemento da página da Web que possui o atributo de identificação "email".

🌐Para automação da web, o identificador de elemento da web pode ser o seletor XPath, o CSS ou os seguintes atributos - id, nome, classe, título, rótulo da ária, text (), href, em ordem decrescente de prioridade. Recomenda escrever XPath manualmente ou simplesmente usando atributos. Há uma espera automática para que um elemento apareça antes que o tempo limite ocorra e é retornado um erro indicando que o elemento não pode ser encontrado. Para alterar o tempo limite padrão de 10 segundos, use a função timeout ().

📸Um identificador de elemento também pode ser um instantâneo de imagem .png ou .bmp que representa o elemento da interface do usuário (pode ser em aplicativos de desktop, janela de terminal ou navegador da web). Se o arquivo de imagem especificado não existir, o OCR será usado para procurar esse texto na tela para atuar no elemento da interface do usuário que contém o texto, por exemplo, r.click ('Submit Form.png'). A transparência (0% de opacidade) é suportada em imagens .png. As coordenadas x, y de elementos na tela também podem ser usadas.

📄Um outro exemplo de identificador de imagem é uma imagem da janela (visualizador de PDF, MS Word, caixa de texto etc.) com o conteúdo central da imagem definido como transparente. Isso permite o uso de read () e snap () para executar o OCR e salvar instantâneos de janelas, contêineres, quadros, caixas de texto de aplicativos com conteúdo variado. Também para o par de coordenadas read () e snap (), x1, y1, x2, y2 pode ser usado para definir a região de interesse na tela para executar o OCR ou capturar instantâneos.

## Funções no núcleo

Função| Parâmetros | Objetivo
------|------------|-----------
 init() | visual_automation = False, chrome_browser= True | inicie o TagUI, configuração automática na primeira execução
 close()| | fechar TagUI, navegador Chrome, SikuliX
 pack()| | para implantar pacote
 update()| | para atualizar pacote sem internet


## Funções Básicas 

Função| Parâmetros | Objetivo
------|------------|-----------
 url()| webpage_url (nenhum parâmetro para retornar o URL atual)|vá para o URL da web
 click()| element_identifier (ou x, y usando automação visual)|clique esquerdo no elemento
 rclick()| element_identifier (ou x, y usando automação visual)|clique com o botão direito do mouse no elemento
 dclick()| element_identifier (ou x, y usando automação visual)| clique duas vezes no elemento
 hover() |element_identifier (ou x, y usando automação visual)|mover o mouse para o elemento
 type() | identificador do elemento (ou x, y), texto_para_tipo ('[enter]', '[clear]')| insira texto no elemento
 select()|  identificador do elemento (ou x, y), valor da opção (ou x, y)| escolha a opção suspensa
 read()| identificador do elemento (página = página da web) (ou x1, y1, x2, y2)| buscar e retornar texto do elemento
 snap()| element_identifier (página = página da web), filename_to_save| salvar captura de teka em arquivo
 load() | filename_to_load | carregar e retornar conteúdo do arquivo
 dump() | text_to_dump, filename_to_save | salvar texto em arquivo
 write() | text_to_write, filename_to_save | anexar texto ao arquivo
 ask()| text_to_prompt | perguntar e retornar a entrada do usuário


## Função Pro
Função| Parâmetros | Objetivo
------|------------|-----------
 keyboard() | keys_and_modifiers (usando automação visual) | enviar pressionamentos de teclas para a tela
 mouse() | 'down' ou 'up' (usando automação visual)	| enviar evento do mouse para a tela
 wait() |  delay_in_seconds (padrão 5 segundos) | explicitamente esperar por algum tempo
 table() | element_identifier (apenas XPath), filename_to_save| salvar tabela HTML básica em CSV
 upload() | element_identifier (apenas CSS), filename_to_upload| fazer upload de arquivo para o elemento web
 download() | download_url, filename_to_save (opcional)| baixar do URL para o arquivo
 unzip() | file_to_unzip, unzip_location (opcional)| descompacte o arquivo zip no local especificado
 frame() | ID ou nome do main_frame, sub_frame (opcional)| definir web frame, frame () para redefinir
 popup() | string_in_url (nenhum parâmetro para redefinir para a página principal)| definir contexto para a guia pop-up da web
 run()| command_to_run (use; entre comandos)| executar comando do SO e retornar saída
 dom() | statement_to_run (código JS a ser executado no navegador)| executar código no DOM e retornar saída
 vision() | command_to_run (código Python para SikuliX)| executar comandos personalizados do SikuliX 
 timeout() | timeout_in_seconds (em branco retorna o tempo limite atual)	| alterar tempo limite de espera (padrão 10s) 

## Função de Ajuda

Função| Parâmetros | Objetivo
------|------------|-----------
 exist() | element_identifier| retornar True ou False se o elemento existir antes do tempo limite
 present() | element_identifier| retornar True ou False se o elemento estiver presente agora
 count() | element_identifier| retorna o número de elementos da web como inteiro 
 clipboard() | text_to_put ou nenhum parâmetro| colocar texto ou retornar texto da área de transferência como string
 mouse_xy() | | retornar '(x, y)' coordenadas do mouse como string
 mouse_x() | | retornar x coordenada do mouse como inteiro
 mouse_y() | | retornar y coordenada do mouse como inteiro
 title() | | retornar o título da página da web atual como string
 text() | | retornar o conteúdo de texto da página da web atual como string
 time() | | tempo de retorno decorrido em segundos entre as chamadas como float


### ORIGINAL 
https://github.com/tebelorg/RPA-Python

#### Tradução: Lorena Guedes





