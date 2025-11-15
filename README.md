# Atividade-Individual---Tema-Caixa-Branca-Parte-1


<h2>NOTAÇÃO DE GRAFO DE FLUXO</h2>
<img width="629" height="777" alt="Generated Image" src="https://github.com/user-attachments/assets/649d801b-50db-46d0-9a74-3d979895443b"/><br>


- **N1** – Início do método  
- **N2** – conectarBD()  
- **N3** – Monta SQL  
- **N4** – st = conn.createStatement()  
- **N5** – rs = st.executeQuery(sql)  
- **N6** – Decisão: rs.next()? (diamond)  
- **N7** – result = true; nome = rs.getString("nome");  
- **N8** – return result  
- **N9** – catch (Exception) - bloco de exceção

### Arestas enumeradas
As arestas (setas) no grafo seguem a ordem:  
1. N1 -> N2  
2. N2 -> N3  
3. N3 -> N4  
4. N4 -> N5  
5. N5 -> N6  
6. N6 (true) -> N7  
7. N6 (false) -> N8  
8. N7 -> N8  
9. N4 -> N9 (possível exceção em createStatement)  
10. N5 -> N9 (possível exceção em executeQuery)


## Cálculo da complexidade ciclomática

Fórmula usada: **M = E − N + 2P**, onde P = número de componentes conectados (P = 1).

- Número de nós (N): 9 (N1..N9).  
- Número de arestas (E): 10 (listadas acima).  
- P = 1.

Cálculo passo a passo:
1. E − N = 10 − 9 = 1  
2. 1 + 2P = 1 + 2×1 = 3

**Complexidade ciclomática M = 3**

Isso indica que **mínimo 3 casos de teste** são necessários para cobrir todos os caminhos independentes.

---


## Caminhos básicos (casos de teste mínimos)

1. **Caminho 1 — sem resultado (rs.next() == false):**  
   1 → 2 → 3 → 4 → 5 → 6(false) → 8

2. **Caminho 2 — usuário encontrado (rs.next() == true):**  
   1 → 2 → 3 → 4 → 5 → 6(true) → 7 → 8

3. **Caminho 3 — exceção (por exemplo: BD inacessível):**  
   1 → 2 → 3 → 4 → 5 → 9 → 8
