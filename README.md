# Atividade-Individual---Tema-Caixa-Branca-Parte-1
<img width="1187" height="665" alt="image" src="https://github.com/user-attachments/assets/b2561218-a2b0-4748-b792-207ba63180b1" />

<h2>NOTAÇÃO DE GRAFO DE FLUXO</h2>

<p>
Nó 1 (Início/Preparação): Início do método, inicialização de sql e conn, e chamada de conectarBD().

Nó 2 (Instrução SQL): Construção da query SQL (linhas 23-26).

Nó 3 (Decisão/Try): Início do bloco try.

Nó 4 (Execução SQL): Criação da Statement e execução da query (executeQuery(sql)).

Nó 5 (Decisão/If): Condicional if (rs.next()) (linha 30).
</p>
<h2>COMPLEXIDADE CICLOMÁTICA</h2> 

Agora aplicamos os valores de E, N, e P na fórmula:M = E - N + 2P Onde: E = 7N = 6P = 1 (para um único método/componente) M = 7 - 6 + 2 \times 1M = 1 + 2\mathbf{M = 3}


<h2>CAMINHO BÁSICO</h2>
Caminho A (Verdadeiro): Se rs.next() for verdadeiro.

Nó 6 (Ação Verdadeira): Atribuição de result = true e obtenção do nome (linhas 30-31).

Retorna ao nó de junção (Nó 7).

Caminho B (Falso): Se rs.next() for falso.

Vai diretamente para o nó de junção (Nó 7). Nó 7 (Junção/Fim do Try): Ponto onde os caminhos do if se unem antes do catch ou fim do try.

Nó 8 (Decisão/Catch): Bloco catch (linha 33) — representa um caminho alternativo se uma Exception for lançada nas linhas 27-32.

Nó 9 (Fim/Return): Retorno de result (linha 34).

Representação em Tópicos:

Vértices (Nós): 9

Arestas (Setas): (1, 2), (2, 3), (3, 4), (4, 5), (5, 6), (5, 7), (6, 7), (3, 8), (4, 8), (5, 8), (6, 8), (7, 8), (7, 9), (8, 9).

