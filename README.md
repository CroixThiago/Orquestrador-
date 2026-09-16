# Kit de Skills do Thiago

Este repositório reúne quatro Claude Skills nascidas da biblioteca pessoal de prompts de Thiago — prompts que ele já usava separadamente, em documentos Word distintos, para orientar pesquisa acadêmica, curadoria de entrevistas e desenvolvimento de produto. O trabalho aqui não foi copiar cada prompt como está: foi ler cada um com cuidado, entender o método por trás dele, agrupar os que compartilham o mesmo motor de raciocínio num só lugar, e devolver isso no formato de Skill que o Claude sabe carregar e seguir sozinho, sem precisar colar o prompt inteiro toda vez.

Cada skill vive na sua própria pasta dentro de `skills/`, com um único arquivo `SKILL.md` — frontmatter (`name` e `description`) mais o corpo de instruções. A `description` é o que decide quando aquela skill entra em ação: escreva-a (ou deixe como está) pensando em como o Claude vai reconhecer a situação.

## As quatro skills

### `orientador-hierarquico`

A mais ampla das quatro. Nasceu da fusão de quatro instrumentos que Thiago usava separados — um editor-apurador hierárquico, um stress-test científico ao estilo Popper/Duhem-Quine, um editor de reescrita em tom jornalístico e um reconstrutor de títulos — todos construídos sobre o mesmo motor de hierarquia decimal (TEMA → SUBTEMA → RECORTE → DETALHAMENTO → MICROANÁLISE) e o mesmo compromisso antialucinação (todo enunciado carrega estatuto: DECLARADO, DERIVADO ou LACUNA COM DONO), estendido depois para tratar regra normativa (ABNT) com o mesmo rigor: nenhuma edição de norma é aplicada de memória sem verificação nesta sessão.

Serve para qualquer texto hierárquico — de um artigo corriqueiro a uma tese de pós-doutorado — e também para livros inteiros, sempre começando por diálogo, nunca produzindo de supetão. Cobre nove modos internos: pesquisar/escrever (R), titular (T), criticar/stress-test de conteúdo (C), reescrever em tom jornalístico (J), auditar texto colado (A), curar e fechar a bibliografia (B), curar o glossário e a consistência terminológica entre capítulos de uma mesma obra (G), fiscalizar conformidade ABNT com a edição vigente da norma (N), e simular uma banca de arguição oral em três papéis (V). Inclui uma seção específica para quando a pessoa chega sem nada pronto ainda — só uma ideia, uma vontade, um sonho — porque nem todo mundo começa já com um artigo ou uma bibliografia nas mãos, e um modelo fixo de referência bibliográfica ancorado em exemplos reais de Thiago para toda citação e lista de referências que a skill produzir. O checklist estilístico também cobre dois marcadores tipográficos: todo termo-chave técnico ou teórico vem em negrito na primeira aparição de cada seção, e toda palavra ou expressão fora do idioma nativo do documento vem em itálico com a definição entre parênteses na primeira ocorrência. A etapa de busca do modo R segue a mesma hierarquia de qualidade de fontes usada para criticar um texto pronto, nomeia poços de dados institucionais por tema (IBGE, Banco Central, Portal de Periódicos CAPES, SciELO, entre outros) e rastreia citações para trás e para frente a partir das fontes mais centrais; todo número derivado por cálculo é reexecutado computacionalmente antes de publicar, quando há ferramenta disponível na sessão.

### `curador-entrevistas-situacionais`

Baseada em dois prompts complementares — um para criar entrevistas situacionais do zero, outro para revisar e lapidar entrevistas já escritas. O método comum: transformar perguntas técnicas em situações do cotidiano, para que a pessoa entrevistada sinta que está contando uma história, não preenchendo formulário. Nasceu do projeto de digitalização de um terreiro, mas o método se aplica a qualquer um dos negócios de Thiago em que o conhecimento relevante mora só na cabeça de alguém que nunca o organizou.

Tem dois modos — Criar e Ajeitar — e um limite inviolável em ambos: antes de qualquer coisa, a skill pergunta qual é, naquele projeto específico, o equivalente ao que a versão original chamava de "proteção cultural" (segredo industrial, dado sensível, o que for) para nunca ser levada a expor isso.

### `motor-produto-em-po`

Baseada no prompt "Diverse Commerce Powder Engine", um fluxo travado por etapas para transformar uma receita em produto comercial em pó para marketplace (Shopee e afins): coleta → análise sensorial → precificação → pacote comercial completo (título, gatilhos psicológicos, posicionamento, palavras-chave, embalagem). Nunca avança de etapa sem aprovação explícita, e nunca inventa dado técnico que exigiria laudo ou análise real (tabela nutricional, shelf life, composição química).

### `pipeline-design-system`

A mais extensa: conduz a criação de um Design System completo, do material bruto anexado até o `Design.md` final, atravessando 15 estágios especializados (auditoria, contexto, pesquisa estratégica, pesquisa de mercado, estratégia visual, linguagem visual, cor, tipografia, tokens, componentes, acessibilidade, layout, motion, governança e consolidação final). Cada estágio decide só o que é seu — nunca redecide o que um estágio anterior já decidiu, nunca antecipa o que caberá a um estágio seguinte — e termina com um bloco de handoff que o próximo consome sem precisar reler tudo do zero. O estágio final resolve conflitos entre especialistas por uma ordem de precedência fixa e documentada.

## Como instalar

Cada pasta dentro de `skills/` é uma Skill completa e autocontida. Para usá-la em uma sessão do Claude (Claude Code, Cowork, ou qualquer ambiente que suporte Skills), copie a pasta correspondente para o diretório de skills do seu projeto ou conta — o próprio Claude reconhece a `description` do frontmatter e carrega o `SKILL.md` quando a situação combina com ela. Não é necessário invocar a skill pelo nome: ela dispara sozinha quando o pedido casa com a descrição.

## Origem

Todo o conteúdo aqui foi sintetizado a partir de prompts que Thiago escreveu e usava manualmente, colando-os inteiros a cada nova conversa. O objetivo deste kit é eliminar essa repetição: o método continua sendo o dele, só que agora carregado automaticamente pelo Claude sempre que a situação pedir.
