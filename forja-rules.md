\# Regras Obrigatórias — Forja de Documentos (The Jedi Order)

Você está trabalhando no sistema de automação de petições do Escritório de Assistência Jurídica (EAJ/UNAERP). Siga rigorosamente estas restrições em todas as alterações:

\#\# 1\. Fontes Autorizadas (Escopo Fechado)  
\- \*\*Modelos Base (\`.docx\`):\*\* Todo documento gerado deve partir obrigatoriamente de um dos templates existentes na pasta \`modelos/\` (\`habilitacao.docx\`, \`procuracao.docx\`, \`gratuidade.docx\`, \`contestacao.docx\`, \`desbloqueio.docx\`, \`citacao\_edital.docx\`, \`intimacao\_pessoal.docx\`, \`penhora\_sisbajud.docx\`, \`oficio\_localizar.docx\`, \`inicial.docx\`, \`contestacao\_pai.docx\`)\[cite: 1, 2\].  
\- \*\*Manual de Referência (\`livro\`):\*\* O arquivo \`livro\` (Prática Cível da Defensoria Pública, localizado na raiz do projeto ou em \`modelos/\`) é a fonte oficial de consulta doutrinária e prática. A IA deve consultá-lo para fundamentar adaptações de teses, pedidos, requisitos legais e adequações de polo (pai/mãe, autor/réu).  
\- \*\*Proibição de Criação Livre:\*\* \*\*NUNCA\*\* gere petições do zero fora dos templates \`.docx\` e \*\*NUNCA\*\* invente números de processos, acórdãos, súmulas ou ementas que não constem nos próprios \`.docx\` ou no arquivo \`livro\`.

\#\# 2\. Papel da IA Conversacional  
\- Identificar qual modelo \`.docx\` do banco se aplica ao caso relatado pelo estagiário;  
\- Consultar o \`livro\` sempre que houver dúvida prática, necessidade de adequação de tese ou ajuste entre polos (ex.: inverter argumentos de mãe para pai);  
\- Coletar apenas as variáveis faltantes em perguntas curtas e objetivas;  
\- Reescrever somente os trechos adaptáveis do caso (gênero, polo processual, narrativa fática e pedidos pontuais), mantendo intacta a estrutura do \`.docx\`.

\#\# 3\. Preservação de Funcionalidades Existentes no \`index.html\`  
Não remova nem quebre nenhuma das seguintes regras já implementadas:  
\- Layout espacial dark/gold/cyan com cabeçalho \`modelos/cabecalho.png\` e fontes \`Cinzel\` e \`Inter\`\[cite: 2\].  
\- Sistema de áudio (\`modelos/som-jedi.mp3\` ao gerar e \`modelos/abertura.mp3\` limitado a 26 segundos no duplo clique do Holocron)\[cite: 2\].  
\- Validação de usuários nas listas \`PADAWANS\` e \`SITHS\` (botão vermelho no modo Sith e bloqueio para nomes fora da lista de padawans).  
\- Easter egg da \*\*Ordem 66\*\* ao digitar \`66\` ou \`66ª\` no campo de Vara.  
\- Toast de café após 30 segundos de inatividade (\`idle-toast\`).  
\- Geração client-side via \`PizZip\` \+ \`Docxtemplater\` \+ \`FileSaver\` e envio do log para \`URL\_PLANILHA\_JEDI\`.

\#\# 4\. Segurança de Chaves de API  
\- Como o front-end é hospedado no GitHub Pages, \*\*NUNCA\*\* insira chaves de API no \`index.html\`\[cite: 2\]. Toda comunicação com a API do Gemini deve passar pelo Google Apps Script (\`URL\_PLANILHA\_JEDI\`).  
