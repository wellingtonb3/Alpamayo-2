# Simulador Alpamayo 2 Edge (demo educacional)

Demo web interativa inspirada no [NVIDIA Alpamayo 2 Edge](https://huggingface.co/nvidia/Alpamayo2-Edge), um modelo VLA (Vision-Language-Action) para direção autônoma.

**Não executa o modelo real.** O carro é guiado por um planejador simples baseado em regras; a demo reproduz o *formato* de entrada e saída do modelo:

- Entrada: 6 câmeras (22 quadros por inferência), 20 poses de histórico e instrução de navegação em texto.
- Saída: trajetória de 64 waypoints (6,4 s) e, quando necessário, raciocínio Chain-of-Causation com nota do AlpaJudge (simulado).

Recursos: eventos provocados (pedestre, corte de faixa, freada brusca, obra), clima, perfis de frota, modo de raciocínio adaptativo e perguntas livres.

## Modo "Você pilota"

Em **Modo de condução**, escolha **Você pilota**:

- ↑/W acelera, ↓/S freia, ←/A e →/D trocam de faixa, Espaço é o freio forte (ou segure os botões na tela).
- Na visão de cima, a linha branca pontilhada é o seu caminho e a linha verde/amarela é o que o modelo faria.
- O painel mostra a sugestão do modelo, a % de concordância, as intervenções do assistente e os sinais vermelhos avançados.
- Com o **assistente de segurança** ligado, o modelo freia por você e bloqueia trocas de faixa perigosas; desligue para dirigir sem rede de proteção.

## Som

Som gerado no próprio navegador (Web Audio, sem arquivos): motor e vento acompanham a velocidade, chuva, seta na troca de faixa, bip quando o modelo raciocina, alarme quando o assistente intervém e som de batida. Tecla **H** buzina. Botão **Som ligado/desligado** e volume no painel Simulação. O áudio começa no primeiro clique na página (regra dos navegadores).

## Como abrir

Arquivo único, sem dependências: abra `index.html` direto no navegador (duplo clique).
