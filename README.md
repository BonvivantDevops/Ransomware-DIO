# Projeto Ransomware e Keylogger em python- DIO
Esse projeto foi desenvolvido para fins educacionais e acadêmicos em ambiente controlado. O uso desses scripts para atacar sistemas sem consentimento prévio é ilegal e antiético.

#Ferramentas e Bibliotecas Utilizadas
Python
Criptografia (Fernet): Para implantação da criptografia simétrica.
Pynput: Para captura de eventos do teclado.
google account: Para receber e-mails

#Keylogger (Captura de Teclas)
O script monitora o teclado do usuário, registra o conteúdo em um arquivo de log local e envia para o email atacante.

keylogger.pyw
Utiliza uma biblioteca pynput para ouvir eventos de imprensa (tecla expressiva).
Tratamento de Dados: Formata teclas especiais (Espaço, Enter, Tab) para controlar o texto legível e ignorar as técnicas de controle (Shift, Ctrl, Alt) para evitar poluição visual.
Salva tudo em tempo real no arquivo log.txt.
keylogger_ em.py
Exfiltração via E-mail: Estende a funcionalidade básica inteira a biblioteca smtplib para envio de dados via protocolo SMTP.
Ciclos de Reporte: Configurado para acumular as teclas e enviar o log por e-mail em intervalos regulares (a cada 30 segundos), simulando o roubo ativo de credenciais.

#Reflexão sobre Defesa Keylogger

1-Múltiplo Fator de Autenticação (MFA): Mesmo que o keylogger capture a senha digitada, o atacante não terá o código do token (celular/app), impedindo o acesso à conta.

2- Teclados Virtuais: Em sites bancários, o uso do mouse para clicar nas teclas evita que o pynput ou hooks de teclado capturem a senha.

3- Monitoramento de Processos: Verificar o Gerenciador de Tarefas por processos suspeitos (muitas vezes com nomes genéricos como python.exe ou svchost.exe rodando fora do padrão) ajuda na detecção.
