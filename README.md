# registro-presenca-google-sheets
Sistema de registro de presença integrado com Google Sheets usando Apps Script

Sistema de Registro de Presença com Google Sheets
Este projeto é uma aplicação web para registro de presença em cursos, utilizando Google Sheets como banco de dados e Google Apps Script para criar uma interface web simples e funcional.
Mostrar Imagem
Características

Interface web simples para registro de presença
Integração com Google Sheets para armazenamento de dados
Lista suspensa de alunos e matérias obtidas diretamente da planilha
Validação de data e horário (apenas permite registros aos domingos entre 17:00 e 19:10)
Evita registros duplicados do mesmo aluno no mesmo dia
Facilmente personalizável e extensível

Pré-requisitos

Conta do Google
Acesso ao Google Drive e Google Sheets
Permissões para usar o Google Apps Script

Configuração
1. Preparar a planilha

Crie uma nova planilha no Google Sheets
Crie duas abas:

Uma aba chamada nomes com:

Coluna A: Nomes dos alunos
Coluna B: Nomes das matérias


Uma aba chamada presenças com os cabeçalhos:

nome | data | horário | matéria





2. Configurar o Google Apps Script

Na sua planilha, vá em Extensões > Apps Script
Crie um novo arquivo de script e nomeie-o como Code.gs
Copie e cole o código do arquivo Code.gs
Crie um novo arquivo HTML clicando em + ao lado de "Arquivos" e selecione "HTML"
Nomeie o arquivo como Index (com "I" maiúsculo) e cole o código do arquivo Index.html
No arquivo Code.gs, substitua 'SUBSTITUA_PELO_ID_DA_SUA_PLANILHA' pelo ID da sua planilha

O ID da planilha está na URL: https://docs.google.com/spreadsheets/d/[SEU-ID-DA-PLANILHA]/edit



3. Publicar como aplicativo web

Clique em Implantar > Nova implantação
Selecione Tipo > Aplicativo da Web
Configure:

Descrição: "Sistema de Registro de Presença"
Executar como: "Eu" (sua conta)
Quem pode acessar: "Qualquer pessoa" (para acesso público) ou "Qualquer pessoa com o link do Google" (para acesso mais restrito)


Clique em Implantar
Copie a URL do aplicativo web e compartilhe com os participantes do curso

Personalizações
Alterar o horário permitido
Para alterar o horário em que a presença pode ser registrada, modifique as linhas no arquivo Code.gs:
javascript// Verificar se é domingo (0) e está entre 17:00 (17.0) e 19:10 (19.1667)
if (diaDaSemana !== 0 || horaAtual < 17.0 || horaAtual > 19.1667) {
Alterar o dia da semana
Para permitir registros em outros dias da semana, modifique o valor da verificação diaDaSemana !== 0:

0: Domingo
1: Segunda-feira
2: Terça-feira
3: Quarta-feira
4: Quinta-feira
5: Sexta-feira
6: Sábado

Contribuições
Contribuições são bem-vindas! Sinta-se à vontade para:

Fazer um fork do projeto
Criar uma branch para sua feature (git checkout -b feature/nova-funcionalidade)
Commitar suas mudanças (git commit -m 'Adiciona nova funcionalidade')
Fazer push para a branch (git push origin feature/nova-funcionalidade)
Abrir um Pull Request

Licença
Este projeto está licenciado sob a licença MIT - veja o arquivo LICENSE para detalhes.
Contato
Jéssica Moraes Siqueira - moraes.jessicas@hotmail.com
Link do Projeto: https://github.com/seu-usuario/registro-presenca-google-sheets
