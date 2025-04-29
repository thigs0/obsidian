- Tema de [[rasterização]]
- Objetivo: determinar quais pixels na tela devem ser coloridos


***Por varredura***
- Definimos uma variável de bit 0
Quando queremos preencher a forma, mudamos o bit para 1 e preenchemos, para isso temos os vértices e definimos com base neles se estamos no interior ou não

**Problemas**
- Dificuldade em analisa formas pontiagudas
- Dificuldade em formas com auto-intersecção

```julia
using Plots

screen = ones(500, 500)
poli = [50 100;
		100 100;
		50 150;
		100 150]
bit = 0
function range(x)
	xmin, xmax= minimum(poli[:, 1]), maximum(poli[:, 1])
	ymin, ymax= minimum(poli[:, 2]), maximum(poli[:, 2])
	
	for j = 1:size(screen)[2]
		if x >= xmin && x <= xmax && j >= ymin &&  j<= ymax
			screen[x, j] = 30
		end
	end
end

anim = @animate for x = 1:size(screen)[1]
	range(x)
end
gif(anim, "test.gif', fps=2)

heatmap(screen, color= :greys)
```

