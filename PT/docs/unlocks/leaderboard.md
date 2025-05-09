# Leaderboard
Se você chegou até aqui, superou muitos desafios. Mas você os resolveu de forma eficiente?
Você pode competir com outros jogadores em vários leaderboards para os métodos de cultivo mais eficientes.

Você pode iniciar uma corrida no leaderboard chamando `leaderboard_run(leaderboard, filename, speedup)`.
Isso inicia uma [simulação](docs/unlocks/simulation.md) semelhante a `simulate()`, exceto que as condições iniciais são fixas. Cada categoria do leaderboard tem diferentes condições de início e sucesso.

A corrida no leaderboard tem sucesso se a condição de sucesso for `True` quando a simulação terminar. A simulação não terminará automaticamente quando o objetivo for alcançado. Você deve garantir que o programa termine.
Se a corrida for bem-sucedida, seu tempo será adicionado ao leaderboard.

Para reduzir a variabilidade, todas as corridas precisam durar pelo menos 2 horas (Você pode acelerar, então não vai demorar tanto). Se uma corrida for completada mais cedo, ela será repetida até alcançar um tempo total de 2 horas. A média de todas as corridas é então enviada como sua pontuação.

Aqui está um exemplo de configuração que o colocará no leaderboard de feno.
![](LeaderboardSetup400)

## Reset Mais Rápido
O reset mais rápido é a categoria mais prestigiada. Automatize completamente o jogo de um único terreno de fazenda para desbloquear os leaderboards novamente.

Você não precisa desbloquear tudo, apenas tente desbloquear o `Unlocks.Leaderboard` o mais rápido possível.

Lembre-se de que você pode usar `num_unlocked(unlock) > 0` para verificar se algo está desbloqueado e pode usar `get_cost()` em desbloqueios para ver quanto custam, assim você pode cultivar automaticamente os itens certos.

Chamada de Função:
`leaderboard_run(Leaderboards.Fastest_Reset, filename, speedup)`

Simulação Equivalente:
`unlocks = {}
items = {}
globals = {}
#um valor de seed negativo significa um seed aleatório
seed = -1
simulate(filename, unlocks, items, globals, seed, speedup)`

Condição de Sucesso:
`num_unlocked(Unlocks.Leaderboard) > 0`

## Labirinto
Comece com tudo desbloqueado e cultive `300000` ouro o mais rápido que puder. Este é exatamente o valor de ouro que você ganhará ao resolver um labirinto `300` vezes.

Chamada de Função:
`leaderboard_run(Leaderboards.Maze, filename, speedup)`

Simulação Equivalente:
`unlocks = Unlocks
items = {Items.Weird_Substance : 1000000, Items.Power: 1000000}
globals = {}
seed = -1
simulate(filename, unlocks, items, globals, seed, speedup)`

Condição de Sucesso:
`num_items(Items.Gold) >= 300000`

## Dinossauro
Comece com tudo desbloqueado e colete `98010` ossos o mais rápido que puder. Este é exatamente o número de ossos que você obterá se preencher uma área de 10x10 com a cauda do dinossauro.

Chamada de Função:
`leaderboard_run(Leaderboards.Dinosaur, filename, speedup)`

Simulação Equivalente:
`unlocks = Unlocks
items = {Items.Pumpkin : 1000000, Items.Power: 1000000}
globals = {}
seed = -1
simulate(filename, unlocks, items, globals, seed, speedup)`

Condição de Sucesso:
`num_items(Items.Bone) >= 98010`

## Outros Leaderboards de Recursos
Cada planta tem seu próprio leaderboard para cultivar essa planta específica o mais rápido possível. Você começa com todos os desbloqueios, os recursos necessários para cultivar a planta e muita energia. O objetivo é cultivar `100000` do recurso produzido pela planta.

Chamadas de Função:
`leaderboard_run(Leaderboards.Cactus, filename, speedup)`
`leaderboard_run(Leaderboards.Sunflowers, filename, speedup)`
`leaderboard_run(Leaderboards.Pumpkins, filename, speedup)`
`leaderboard_run(Leaderboards.Wood, filename, speedup)`
`leaderboard_run(Leaderboards.Carrots, filename, speedup)`
`leaderboard_run(Leaderboards.Hay, filename, speedup)`
`leaderboard_run(Leaderboards.Polyculture, filename, speedup)`

Condição de Sucesso:
`num_items(resource) >= 100000`

`Leaderboards.Polyculture` requer cultivar `100000` de todos os três recursos de policultura.