# Teste do script vp

## Parte 1 - Casos base

### Teste 1 — -p sem diretórios indicados termina com erro 
![teste1](test_screenshots/teste1.png)

### Teste 2 — -v sem base de dados existente termina com erro 
![teste2](test_screenshots/teste2.png)

### Teste 3 — -p e -v usados em simultâneo termina com erro 
![teste3](test_screenshots/teste3.png)

### Teste 4 — Proteger um diretório com sucesso (mensagem "criada com sucesso")
![teste4](test_screenshots/teste4.png)

### Teste 5 — O ficheiro da base de dados é criado após o -p, e fica sem permissão de escrita (read-only)
![teste5](test_screenshots/teste5.png)

### Teste 7 — Verificação sem alterações reporta tudo como verificado (0 modificados/apagados/novos)
![teste7](test_screenshots/teste7.png)

### Teste 8 — Alteração de conteúdo de um ficheiro é detetada ("Conteúdo")
![teste8](test_screenshots/teste8.png)

### Teste 9 — Ficheiro apagado é detetado ("foi APAGADO")
![teste9](test_screenshots/teste9.png)

### Teste 10 — Ficheiro novo é detetado ("é NOVO")
![teste10](test_screenshots/teste10.png)

### Teste 11 — Exclusão de padrões (-e) ignora ficheiros na proteção e na verificação
![teste11](test_screenshots/teste11.png)

### Teste 12 — Resumo final mostra contagens corretas com múltiplas alterações (modificado + apagado + novo)
![teste12](test_screenshots/teste12.png)

### Teste 13 — Proteger múltiplos diretórios ao mesmo tempo funciona e é refletido no resumo
![teste13](test_screenshots/teste13.png)

### Teste 14 — Proteção falha corretamente quando a BD não pode ser escrita (não reporta falso sucesso)
![teste14](test_screenshots/teste14.png)

### Teste 15 — Proteção falha corretamente quando o diretório indicado não existe
![teste15](test_screenshots/teste15.png)

## Parte 2 - Edge cases

### Teste 16 — Alteração apenas de permissões (chmod) é detetada ("Permissões")
![teste16](test_screenshots/teste16.png)

### Teste 17 — Alteração apenas da data de modificação (touch, sem mudar conteúdo) é detetada
![teste17](test_screenshots/teste17.png)

### Teste 18 — Conteúdo alterado mantendo o mesmo tamanho é detetado (deteção pelo hash, não pelo tamanho)
![teste18](test_screenshots/teste18.png)

### Teste 19 — -v sem -e herda o padrão de exclusão guardado na BD (definido no -p)
![teste19](test_screenshots/teste19.png)

### Teste 20 — -v com -e diferente do usado no -p substitui a exclusão guardada
![teste20](test_screenshots/teste20.png)

### Teste 21 — Exclusão de padrão (-e) aplica-se também a ficheiros em subdiretórios aninhados
![teste21](test_screenshots/teste21.png)

### Teste 22 — -f sem valor a seguir termina com erro (não consome a próxima flag por engano)
![teste22](test_screenshots/teste22.png)

### Teste 23 — -e sem valor a seguir termina com erro
![teste23](test_screenshots/teste23.png)

### Teste 24 — Switch desconhecido (ex. -x) termina com erro e mostra mensagem clara
![teste24](test_screenshots/teste24.png)

### Teste 25 — Flags podem aparecer depois dos argumentos posicionais (ex. "vp dir -p -f db")
![teste25](test_screenshots/teste25.png)

### Teste 26 — Sem -p e sem -v, com diretório posicional dado: comporta-se como -v e ignora o diretório
![teste26](test_screenshots/teste26.png)

### Teste 27 — Exit code de sucesso é 0 tanto na proteção como na verificação
![teste27](test_screenshots/teste27.png)

### Teste 28 — Nomes de ficheiros com espaços são tratados corretamente
![teste28](test_screenshots/teste28.png)

### Teste 29 — Proteger/verificar um diretório vazio (0 ficheiros) funciona sem erros
![teste29](test_screenshots/teste29.png)

### Teste 30 — Subdiretórios aninhados (vários níveis) são percorridos recursivamente
![teste30](test_screenshots/teste30.png)

### Teste 31 — Reproteger substitui uma BD anterior só de leitura, sem ser preciso apagá-la à mão
![teste31](test_screenshots/teste31.png)

### Teste 32 — -f com diretório-pai inexistente no caminho termina com erro (não só quando é um ficheiro a bloquear)
![teste32](test_screenshots/teste32.png)

### Teste 33 — Proteger um diretório que contém a própria BD causa auto-modificação na verificação seguinte
![teste33](test_screenshots/teste33.png)

### Teste 34 — -s emite um alerta via logger quando é detetada uma alteração
![teste34](test_screenshots/teste34.png)

### Teste 35 — Ficheiro sem permissão de leitura é omitido silenciosamente da BD (sem aviso ao utilizador)
![teste35](test_screenshots/teste35.png)
