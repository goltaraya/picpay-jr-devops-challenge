# Desafio DevOps Jr do PicPay - detalhes
Então, eu me empolguei e acabei fazendo tudo em 2 commits hehe mas vamos lá. <br>
Fiz um passo a passo do que eu arrumei (do que eu lembro pelo menos).

## Passo a Passo:
### No arquivo docker-compose.yaml:
1. Criar networks: frontend e backend
2. Corrigir o nome do banco de dados para redis (antes está escrito errado e obviamente o serviço vai rodar, porém não vai comunicar com as apps já que nelas o nome está 'redis').
3. Adicionar os networks criados ao redis e definir a porta padrão do redis (6379).
4. Trocar a porta do serviço web de 5000 para 3000, já que quando rodamos a aplicação, a mesma expõe a porta 3000 para conexão, e não a 5000. Óbviamente você consegue redirecionar esse tipo de porta de 5000 para 3000 MAS como é bom manter o padrão para que futuramente se precisarmos de uma ou outra porta, não haja conflitos.
5. OBSERVAÇÃO: No meu caso, mudei a porta 8080 do writer para 8081 e 8081 do reader para 8082, por motivos da 8080 já estar sendo usada na minha máquina. Vale ressaltar que além de fazer esse tipo de mudança, é necessário mudar também as referências dentro de cada app e Dockerfile para que os serviços consigam se encontrar/comunicar.
