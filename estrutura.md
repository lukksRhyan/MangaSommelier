# CONTEXTO DO PROJETO PARA PROCESSAMENTO DE IA

> **Instrução para a IA:** O documento abaixo contém a estrutura completa e o código-fonte do projeto. Use este mapeamento para entender o fluxo do sistema, arquitetura e dependências.

## Mapeamento de Diretórios (Árvore do Projeto)
```text
site-promos/
├── .git/
│   ├── hooks/
│   │   ├── applypatch-msg.sample
│   │   ├── commit-msg.sample
│   │   ├── fsmonitor-watchman.sample
│   │   ├── post-update.sample
│   │   ├── pre-applypatch.sample
│   │   ├── pre-commit.sample
│   │   ├── pre-merge-commit.sample
│   │   ├── pre-push.sample
│   │   ├── pre-rebase.sample
│   │   ├── pre-receive.sample
│   │   ├── prepare-commit-msg.sample
│   │   ├── push-to-checkout.sample
│   │   ├── sendemail-validate.sample
│   │   └── update.sample
│   ├── info/
│   │   └── exclude
│   ├── logs/
│   │   ├── refs/
│   │   │   ├── heads/
│   │   │   │   └── main
│   │   │   └── remotes/
│   │   │       └── origin/
│   │   │           └── main
│   │   └── HEAD
│   ├── objects/
│   │   ├── 00/
│   │   │   └── bea410118aa466bb0069f8cb17f6ba96026054
│   │   ├── 02/
│   │   │   └── b0da16663c5045341d3681c52d5bcee91fac6c
│   │   ├── 04/
│   │   │   └── fb1753c0ce09bacfd3d63bd41ebe95dda29931
│   │   ├── 0d/
│   │   │   ├── 16df1c58b1d824bcf405627f0e7b7c12dd87de
│   │   │   └── 5ba7216595e32ef3d834788467800ccc6a3377
│   │   ├── 0f/
│   │   │   └── 6c580aa9791e8f000f6e6abcd8f4b7859134b3
│   │   ├── 1e/
│   │   │   └── 4c569ab13b4ad885304093ee2c6eb0a05d1fa8
│   │   ├── 21/
│   │   │   └── 207c7833beb663839474f3e03485ab331472d3
│   │   ├── 25/
│   │   │   ├── 4c7ee0814999814e3094dcf9d9d89fa4cfae50
│   │   │   └── 5392d93c88e58ea50d6acdf2ada23fa374d277
│   │   ├── 26/
│   │   │   └── a98f670727be7cebf83699bf572a37f56f1e75
│   │   ├── 28/
│   │   │   ├── 65d6658fb520a7c52795d592d04b654bbaf67e
│   │   │   └── 9388cd964599bfcafc60363cdd120f79ffa07b
│   │   ├── 2c/
│   │   │   └── da26733c2f376abf5e998570afcb918b7d205c
│   │   ├── 2e/
│   │   │   └── c0a027d3ea47c0620cf9536888aa47d2c4cd9e
│   │   ├── 31/
│   │   │   └── b6d326ee36d38d44a0e4d1837053a8a316a096
│   │   ├── 33/
│   │   │   └── 15f8df7eaca06c2a19655c7be4873ee565b7a2
│   │   ├── 3a/
│   │   │   └── 132806fc3424d93dc0c878cdc38bdd878b6640
│   │   ├── 43/
│   │   │   └── 90f96a5008728a9e329cc9d01b54f0d3d924d3
│   │   ├── 44/
│   │   │   └── 0d52ec278b3f2f82ad97cc387c46109d1b0962
│   │   ├── 51/
│   │   │   └── d71ad4d6b9903712b0837e770a6e06c92081cf
│   │   ├── 52/
│   │   │   ├── 29ac79058d55669fdac8145efbc94a61564128
│   │   │   ├── 61aeca86f46b0438c1c0aeaf6a60cc38597f2c
│   │   │   └── fbd19d52d5c69b30b7204044c0284b9e711563
│   │   ├── 57/
│   │   │   └── f229201a44ee6f7745c51f1f2610e7c254fc01
│   │   ├── 59/
│   │   │   └── b3020ebb152870515f74966e013ae1e8988fbf
│   │   ├── 61/
│   │   │   └── 96fc42ba24e0d8ee2fb0d7d5a5166068bd4a1f
│   │   ├── 65/
│   │   │   └── a112d20396d5c3bca771306e7b406f1ea1a324
│   │   ├── 66/
│   │   │   └── aab072ae98d3b4591e7915b4cf11306702466c
│   │   ├── 6a/
│   │   │   └── 1d7187e9ece2ec222fb4408c4a7239cb9a3686
│   │   ├── 6c/
│   │   │   └── 898533528d30a7d1288cd3575d3cfed2931603
│   │   ├── 6f/
│   │   │   └── 8c28675684c3f9c94c9cd057364315ad4c11a3
│   │   ├── 73/
│   │   │   └── 7503dc934c4947656aa8aaa1b6da460b889d3d
│   │   ├── 76/
│   │   │   └── 7c3d2115a7ecd6638602f4dd2dd7f0c62e2a95
│   │   ├── 77/
│   │   │   └── a0e8069d9ec29c1b9931f8180583035d3017ad
│   │   ├── 7c/
│   │   │   └── bafab6e74326e56986b6936c2b1734e42c2bb2
│   │   ├── 83/
│   │   │   └── 5ec99fa5faf40b18f8314264b6af4229a5aa18
│   │   ├── 96/
│   │   │   ├── e35c718d616baaf1a883d62793ee6764e0adc4
│   │   │   └── fa6298f81c0df167f0c85cd18a5bb9013d5831
│   │   ├── 97/
│   │   │   └── 12ca43494ef2ccfbcda471d5170a606196eacb
│   │   ├── 9e/
│   │   │   └── 2b83b149f35c0241d96c1f24535f647f012916
│   │   ├── 9f/
│   │   │   └── 32a34b5143eea97c8e45796f3e451721d15155
│   │   ├── a1/
│   │   │   └── 4322498bdfec7ec28602916a05f7f0b0601f56
│   │   ├── a3/
│   │   │   └── 83d8704c3923e46d397170b0b9c5be40a0a1b5
│   │   ├── a4/
│   │   │   └── af1ba73a91917aa6295fb07d6cce494fdc8701
│   │   ├── ad/
│   │   │   ├── 725ad88b9c08761a534eb5cc7c251944561ead
│   │   │   └── d486ec011d0424f920e14220907990132199be
│   │   ├── b2/
│   │   │   ├── 767fdb07e7d51eeba990a384dcde4a1a8486da
│   │   │   └── b604acd5fb361f096223462544cf655b8ebf20
│   │   ├── b7/
│   │   │   └── 6524d24385ed257619a866bde384297be94929
│   │   ├── bd/
│   │   │   └── c3bcdd17e5e8c44143fd304ac1d90e6cf3582b
│   │   ├── c3/
│   │   │   ├── 04b916fb3a1ab8bee7ef76ca8d1f6c7f7ab615
│   │   │   └── 4e326c52065b44b23cc48da057b20865cee652
│   │   ├── c6/
│   │   │   └── edaca68bdac96470c758357ecd15a8b48b73ea
│   │   ├── c7/
│   │   │   └── 3329f650ebf9d9796be95d09a9b2f796107769
│   │   ├── d6/
│   │   │   └── 930dca63edc0ba0323bbd5f50ea4c65925c0ac
│   │   ├── dc/
│   │   │   └── 677fc7aa71afbbb3379061bfc2acd6ed74bd70
│   │   ├── de/
│   │   │   ├── afcf2b255a141d0bdced59806a03132921ed07
│   │   │   └── c1ea33aade40ea675d39a4e975f7dd38f49146
│   │   ├── e5/
│   │   │   └── 40d799fc0bf7f248e41150d7cbb181e728ea85
│   │   ├── ee/
│   │   │   └── 926deede46482220f4fda7c71413eb36f45896
│   │   ├── ef/
│   │   │   ├── 0155f353c5913ef1749cb1fc724bb7dba2cb5b
│   │   │   └── 1813e3f4af8be431d4ba39664a3db4a144db60
│   │   ├── fd/
│   │   │   ├── 25cc702355c4adde5ab3f6bf1b41610f3ab39d
│   │   │   └── b9624f6fab1687edf7068f6666f41960fb7d6a
│   │   ├── info/
│   │   └── pack/
│   ├── refs/
│   │   ├── heads/
│   │   │   └── main
│   │   ├── remotes/
│   │   │   └── origin/
│   │   │       └── main
│   │   └── tags/
│   ├── COMMIT_EDITMSG
│   ├── config
│   ├── description
│   ├── FETCH_HEAD
│   ├── HEAD
│   ├── index
│   └── ORIG_HEAD
├── photos/
├── series/
│   ├── 101517/
│   │   └── index.html
│   ├── 111233/
│   │   └── index.html
│   ├── 30012/
│   │   └── index.html
│   ├── 30025/
│   │   └── index.html
│   ├── 30908/
│   │   └── index.html
│   ├── 74489/
│   │   └── index.html
│   ├── 86635/
│   │   └── index.html
│   ├── 98235/
│   │   └── index.html
│   ├── 144866.html
│   ├── 199547.html
│   ├── 30001.html
│   └── index.html
└── index.html
```
---

## Código-Fonte e Conteúdo dos Arquivos

### Arquivo: `index.html`
<file path="index.html" lines="257">
```html

    <!DOCTYPE html>
    <html lang="pt-br">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Mundo Mangá Promos - Mural de Ofertas</title>
        <script src="https://cdn.tailwindcss.com"></script>
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
        <style>
            @import url('https://fonts.googleapis.com/css2?family=Special+Elite&display=swap');
            
            body { 
                background-color: #f3e5d8; 
                color: #57310a; 
                font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            }
            
            .font-vintage { font-family: 'Special Elite', cursive; }
            
            .paper-texture {
                background-color: #fffcf5;
                background-image: url('https://www.transparenttextures.com/patterns/parchment.png');
            }

            .ripped-edge {
                position: relative;
                background: #57310a;
                color: white;
                clip-path: polygon(0% 0%, 100% 0%, 100% 90%, 95% 100%, 90% 90%, 85% 100%, 80% 90%, 75% 100%, 70% 90%, 65% 100%, 60% 90%, 55% 100%, 50% 90%, 45% 100%, 40% 90%, 35% 100%, 30% 90%, 25% 100%, 20% 90%, 15% 100%, 10% 90%, 5% 100%, 0% 90%);
            }
            
            .card-manga {
                border: 2px solid #57310a;
                transition: transform 0.2s;
            }
            
            .card-manga:hover {
                transform: translateY(-5px);
            }

            .social-bar {
                background: rgba(87, 49, 10, 0.9);
                backdrop-filter: blur(5px);
            }
        </style>
    </head>
    <body class="pb-12">
        <nav class="social-bar sticky top-0 z-50 py-3 px-6 text-white flex justify-center gap-8 shadow-md">
            <a href="https://www.tiktok.com/@manga_gourmetbr" target="_blank" class="hover:text-[#f3e5d8] transition-colors flex items-center gap-2">
                <i class="fab fa-tiktok"></i> <span class="hidden sm:inline font-bold">TikTok</span>
            </a>
            <a href="https://www.instagram.com/manga_gourmetbr/" target="_blank" class="hover:text-[#f3e5d8] transition-colors flex items-center gap-2">
                <i class="fab fa-instagram"></i> <span class="hidden sm:inline font-bold">Instagram</span>
            </a>
            <a href="https://www.youtube.com/@MangaGourmet" target="_blank" class="hover:text-[#f3e5d8] transition-colors flex items-center gap-2">
                <i class="fab fa-youtube"></i> <span class="hidden sm:inline font-bold">YouTube</span>
            </a>
        </nav>

        <header class="ripped-edge pt-12 pb-24 px-6 text-center shadow-2xl mb-10">
            <h1 class="text-4xl md:text-6xl font-black uppercase tracking-tighter">Mundo Mangá</h1>
            <p class="text-lg opacity-90 mt-2 font-vintage">Promoções Atualizadas do Dia</p>
            
            <div class="mt-8">
                <a href="series/index.html" class="inline-flex items-center justify-center bg-[#f3e5d8] text-[#57310a] px-8 py-3 rounded-full font-bold uppercase tracking-widest hover:bg-white transition-colors shadow-lg">
                    <i class="fas fa-layer-group mr-2"></i> Ver por Séries
                </a>
            </div>
        </header>

        <main class="max-w-6xl mx-auto px-4 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
            
            <div class="card-manga paper-texture rounded-lg overflow-hidden shadow-lg flex flex-col">
                <div class="h-80 bg-white p-4 flex items-center justify-center">
                    <img src="https://m.media-amazon.com/images/I/61AU5L7LvRL._SY466_.jpg" alt="Haikyu! Vol. 01 - Big" class="max-h-full object-contain">
                </div>
                <div class="p-6 flex-grow border-t-2 border-dashed border-[#57310a] flex flex-col justify-between">
                    <div>
                        <h2 class="text-xl font-bold leading-tight mb-2 uppercase font-vintage">Haikyu! Vol. 01 - Big</h2>
                        <p class="text-3xl font-black text-[#57310a] mb-4">R$27,24 (57%)</p>
                    </div>
                    <a href="https://amzn.to/4sU54qP" target="_blank" 
                       class="block w-full py-4 bg-[#57310a] text-white text-center font-bold rounded-full hover:bg-opacity-90 transition-all uppercase tracking-widest text-sm shadow-md">
                        <i class="fas fa-shopping-cart mr-2"></i> Resgatar Promoção
                    </a>
                </div>
            </div>
            
            <div class="card-manga paper-texture rounded-lg overflow-hidden shadow-lg flex flex-col">
                <div class="h-80 bg-white p-4 flex items-center justify-center">
                    <img src="https://m.media-amazon.com/images/I/61XxuXlATeL._SY425_.jpg" alt="Yu Yu Hakusho - Volume - 1" class="max-h-full object-contain">
                </div>
                <div class="p-6 flex-grow border-t-2 border-dashed border-[#57310a] flex flex-col justify-between">
                    <div>
                        <h2 class="text-xl font-bold leading-tight mb-2 uppercase font-vintage">Yu Yu Hakusho - Volume - 1</h2>
                        <p class="text-3xl font-black text-[#57310a] mb-4">R$20,92 (52%)</p>
                    </div>
                    <a href="https://amzn.to/3PNrOdH" target="_blank" 
                       class="block w-full py-4 bg-[#57310a] text-white text-center font-bold rounded-full hover:bg-opacity-90 transition-all uppercase tracking-widest text-sm shadow-md">
                        <i class="fas fa-shopping-cart mr-2"></i> Resgatar Promoção
                    </a>
                </div>
            </div>
            
            <div class="card-manga paper-texture rounded-lg overflow-hidden shadow-lg flex flex-col">
                <div class="h-80 bg-white p-4 flex items-center justify-center">
                    <img src="https://m.media-amazon.com/images/I/51EQ5jMPsHL._SY425_.jpg" alt="Boa Noite Punpun - Vol. 1" class="max-h-full object-contain">
                </div>
                <div class="p-6 flex-grow border-t-2 border-dashed border-[#57310a] flex flex-col justify-between">
                    <div>
                        <h2 class="text-xl font-bold leading-tight mb-2 uppercase font-vintage">Boa Noite Punpun - Vol. 1</h2>
                        <p class="text-3xl font-black text-[#57310a] mb-4">R$28,09 (57%)</p>
                    </div>
                    <a href="https://amzn.to/4sfebBi" target="_blank" 
                       class="block w-full py-4 bg-[#57310a] text-white text-center font-bold rounded-full hover:bg-opacity-90 transition-all uppercase tracking-widest text-sm shadow-md">
                        <i class="fas fa-shopping-cart mr-2"></i> Resgatar Promoção
                    </a>
                </div>
            </div>
            
            <div class="card-manga paper-texture rounded-lg overflow-hidden shadow-lg flex flex-col">
                <div class="h-80 bg-white p-4 flex items-center justify-center">
                    <img src="https://m.media-amazon.com/images/I/81CBWnhIDPL._SY425_.jpg" alt="Box O castelo animado" class="max-h-full object-contain">
                </div>
                <div class="p-6 flex-grow border-t-2 border-dashed border-[#57310a] flex flex-col justify-between">
                    <div>
                        <h2 class="text-xl font-bold leading-tight mb-2 uppercase font-vintage">Box O castelo animado</h2>
                        <p class="text-3xl font-black text-[#57310a] mb-4">R$68,32 (65%) com o cupom LIVROS20OFF</p>
                    </div>
                    <a href="https://amzn.to/4c6wC57" target="_blank" 
                       class="block w-full py-4 bg-[#57310a] text-white text-center font-bold rounded-full hover:bg-opacity-90 transition-all uppercase tracking-widest text-sm shadow-md">
                        <i class="fas fa-shopping-cart mr-2"></i> Resgatar Promoção
                    </a>
                </div>
            </div>
            
            <div class="card-manga paper-texture rounded-lg overflow-hidden shadow-lg flex flex-col">
                <div class="h-80 bg-white p-4 flex items-center justify-center">
                    <img src="https://m.media-amazon.com/images/I/71bUl1HkkCL._SY466_.jpg" alt="Haikyu!! Vol. 16 - Big" class="max-h-full object-contain">
                </div>
                <div class="p-6 flex-grow border-t-2 border-dashed border-[#57310a] flex flex-col justify-between">
                    <div>
                        <h2 class="text-xl font-bold leading-tight mb-2 uppercase font-vintage">Haikyu!! Vol. 16 - Big</h2>
                        <p class="text-3xl font-black text-[#57310a] mb-4">R$31,95 (50%)</p>
                    </div>
                    <a href="https://amzn.to/4skGZIS" target="_blank" 
                       class="block w-full py-4 bg-[#57310a] text-white text-center font-bold rounded-full hover:bg-opacity-90 transition-all uppercase tracking-widest text-sm shadow-md">
                        <i class="fas fa-shopping-cart mr-2"></i> Resgatar Promoção
                    </a>
                </div>
            </div>
            
            <div class="card-manga paper-texture rounded-lg overflow-hidden shadow-lg flex flex-col">
                <div class="h-80 bg-white p-4 flex items-center justify-center">
                    <img src="https://m.media-amazon.com/images/I/719PH7se9TL._SY425_.jpg" alt="A Prisão no Céu" class="max-h-full object-contain">
                </div>
                <div class="p-6 flex-grow border-t-2 border-dashed border-[#57310a] flex flex-col justify-between">
                    <div>
                        <h2 class="text-xl font-bold leading-tight mb-2 uppercase font-vintage">A Prisão no Céu</h2>
                        <p class="text-3xl font-black text-[#57310a] mb-4">R$26,78 (55%)</p>
                    </div>
                    <a href="https://amzn.to/4tuXNhe" target="_blank" 
                       class="block w-full py-4 bg-[#57310a] text-white text-center font-bold rounded-full hover:bg-opacity-90 transition-all uppercase tracking-widest text-sm shadow-md">
                        <i class="fas fa-shopping-cart mr-2"></i> Resgatar Promoção
                    </a>
                </div>
            </div>
            
            <div class="card-manga paper-texture rounded-lg overflow-hidden shadow-lg flex flex-col">
                <div class="h-80 bg-white p-4 flex items-center justify-center">
                    <img src="https://m.media-amazon.com/images/I/71s4v7f7BWL._SY342_.jpg" alt="Demon slayer - kimetsu no yaiba vol. 11" class="max-h-full object-contain">
                </div>
                <div class="p-6 flex-grow border-t-2 border-dashed border-[#57310a] flex flex-col justify-between">
                    <div>
                        <h2 class="text-xl font-bold leading-tight mb-2 uppercase font-vintage">Demon slayer - kimetsu no yaiba vol. 11</h2>
                        <p class="text-3xl font-black text-[#57310a] mb-4">R$23,95 (50%)</p>
                    </div>
                    <a href="https://amzn.to/4tt3YlV" target="_blank" 
                       class="block w-full py-4 bg-[#57310a] text-white text-center font-bold rounded-full hover:bg-opacity-90 transition-all uppercase tracking-widest text-sm shadow-md">
                        <i class="fas fa-shopping-cart mr-2"></i> Resgatar Promoção
                    </a>
                </div>
            </div>
            
            <div class="card-manga paper-texture rounded-lg overflow-hidden shadow-lg flex flex-col">
                <div class="h-80 bg-white p-4 flex items-center justify-center">
                    <img src="https://m.media-amazon.com/images/I/712Qb-JEWDL._SY466_.jpg" alt="Shangri-la Frontier Vol. 13" class="max-h-full object-contain">
                </div>
                <div class="p-6 flex-grow border-t-2 border-dashed border-[#57310a] flex flex-col justify-between">
                    <div>
                        <h2 class="text-xl font-bold leading-tight mb-2 uppercase font-vintage">Shangri-la Frontier Vol. 13</h2>
                        <p class="text-3xl font-black text-[#57310a] mb-4">R$15,96 (60%)</p>
                    </div>
                    <a href="https://amzn.to/41fNgug" target="_blank" 
                       class="block w-full py-4 bg-[#57310a] text-white text-center font-bold rounded-full hover:bg-opacity-90 transition-all uppercase tracking-widest text-sm shadow-md">
                        <i class="fas fa-shopping-cart mr-2"></i> Resgatar Promoção
                    </a>
                </div>
            </div>
            
            <div class="card-manga paper-texture rounded-lg overflow-hidden shadow-lg flex flex-col">
                <div class="h-80 bg-white p-4 flex items-center justify-center">
                    <img src="https://m.media-amazon.com/images/I/91ZQuMWWh5L._SY466_.jpg" alt="One-punch man - volume 12" class="max-h-full object-contain">
                </div>
                <div class="p-6 flex-grow border-t-2 border-dashed border-[#57310a] flex flex-col justify-between">
                    <div>
                        <h2 class="text-xl font-bold leading-tight mb-2 uppercase font-vintage">One-punch man - volume 12</h2>
                        <p class="text-3xl font-black text-[#57310a] mb-4">R$17,56 (60%)</p>
                    </div>
                    <a href="https://amzn.to/4tPhEYP" target="_blank" 
                       class="block w-full py-4 bg-[#57310a] text-white text-center font-bold rounded-full hover:bg-opacity-90 transition-all uppercase tracking-widest text-sm shadow-md">
                        <i class="fas fa-shopping-cart mr-2"></i> Resgatar Promoção
                    </a>
                </div>
            </div>
            
            <div class="card-manga paper-texture rounded-lg overflow-hidden shadow-lg flex flex-col">
                <div class="h-80 bg-white p-4 flex items-center justify-center">
                    <img src="https://m.media-amazon.com/images/I/71Stz+ZMKtL._SY342_.jpg" alt="Ataque dos titãs vol. 14: série original" class="max-h-full object-contain">
                </div>
                <div class="p-6 flex-grow border-t-2 border-dashed border-[#57310a] flex flex-col justify-between">
                    <div>
                        <h2 class="text-xl font-bold leading-tight mb-2 uppercase font-vintage">Ataque dos titãs vol. 14: série original</h2>
                        <p class="text-3xl font-black text-[#57310a] mb-4">R$21,43 (51%)</p>
                    </div>
                    <a href="https://amzn.to/4sZhn5m" target="_blank" 
                       class="block w-full py-4 bg-[#57310a] text-white text-center font-bold rounded-full hover:bg-opacity-90 transition-all uppercase tracking-widest text-sm shadow-md">
                        <i class="fas fa-shopping-cart mr-2"></i> Resgatar Promoção
                    </a>
                </div>
            </div>
            
            <div class="card-manga paper-texture rounded-lg overflow-hidden shadow-lg flex flex-col">
                <div class="h-80 bg-white p-4 flex items-center justify-center">
                    <img src="https://m.media-amazon.com/images/I/81tLIsqahcL._SY425_.jpg" alt="Old Boy (mangá volume 3 de 3)" class="max-h-full object-contain">
                </div>
                <div class="p-6 flex-grow border-t-2 border-dashed border-[#57310a] flex flex-col justify-between">
                    <div>
                        <h2 class="text-xl font-bold leading-tight mb-2 uppercase font-vintage">Old Boy (mangá volume 3 de 3)</h2>
                        <p class="text-3xl font-black text-[#57310a] mb-4">R$63,74 (50%)</p>
                    </div>
                    <a href="https://amzn.to/4c2MFCx" target="_blank" 
                       class="block w-full py-4 bg-[#57310a] text-white text-center font-bold rounded-full hover:bg-opacity-90 transition-all uppercase tracking-widest text-sm shadow-md">
                        <i class="fas fa-shopping-cart mr-2"></i> Resgatar Promoção
                    </a>
                </div>
            </div>
            
        </main>

        <footer class="mt-20 text-center opacity-60 italic font-vintage">
            <p>@manga_gourmetbr - Links de Associado Amazon</p>
        </footer>
    </body>
    </html>
    
```
</file>

### Arquivo: `.git/COMMIT_EDITMSG`
<file path=".git/COMMIT_EDITMSG" lines="1">
```
marriagetoxinandaakanebanashi

```
</file>

### Arquivo: `.git/config`
<file path=".git/config" lines="13">
```
[core]
	repositoryformatversion = 0
	filemode = false
	bare = false
	logallrefupdates = true
	symlinks = false
	ignorecase = true
[remote "origin"]
	url = https://github.com/lukksRhyan/MangaSommelier.git
	fetch = +refs/heads/*:refs/remotes/origin/*
[branch "main"]
	remote = origin
	merge = refs/heads/main

```
</file>

### Arquivo: `.git/description`
<file path=".git/description" lines="1">
```
Unnamed repository; edit this file 'description' to name the repository.

```
</file>

### Arquivo: `.git/FETCH_HEAD`
<file path=".git/FETCH_HEAD" lines="1">
```
a383d8704c3923e46d397170b0b9c5be40a0a1b5		branch 'main' of https://github.com/lukksRhyan/MangaSommelier

```
</file>

### Arquivo: `.git/HEAD`
<file path=".git/HEAD" lines="1">
```
ref: refs/heads/main

```
</file>

### Arquivo: `.git/index`
<file path=".git/index" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xc6 in position 13: invalid continuation byte>
```
</file>

### Arquivo: `.git/ORIG_HEAD`
<file path=".git/ORIG_HEAD" lines="1">
```
51d71ad4d6b9903712b0837e770a6e06c92081cf

```
</file>

### Arquivo: `.git/hooks/applypatch-msg.sample`
<file path=".git/hooks/applypatch-msg.sample" lines="15">
```sample
#!/bin/sh
#
# An example hook script to check the commit log message taken by
# applypatch from an e-mail message.
#
# The hook should exit with non-zero status after issuing an
# appropriate message if it wants to stop the commit.  The hook is
# allowed to edit the commit message file.
#
# To enable this hook, rename this file to "applypatch-msg".

. git-sh-setup
commitmsg="$(git rev-parse --git-path hooks/commit-msg)"
test -x "$commitmsg" && exec "$commitmsg" ${1+"$@"}
:

```
</file>

### Arquivo: `.git/hooks/commit-msg.sample`
<file path=".git/hooks/commit-msg.sample" lines="24">
```sample
#!/bin/sh
#
# An example hook script to check the commit log message.
# Called by "git commit" with one argument, the name of the file
# that has the commit message.  The hook should exit with non-zero
# status after issuing an appropriate message if it wants to stop the
# commit.  The hook is allowed to edit the commit message file.
#
# To enable this hook, rename this file to "commit-msg".

# Uncomment the below to add a Signed-off-by line to the message.
# Doing this in a hook is a bad idea in general, but the prepare-commit-msg
# hook is more suited to it.
#
# SOB=$(git var GIT_AUTHOR_IDENT | sed -n 's/^\(.*>\).*$/Signed-off-by: \1/p')
# grep -qs "^$SOB" "$1" || echo "$SOB" >> "$1"

# This example catches duplicate Signed-off-by lines.

test "" = "$(grep '^Signed-off-by: ' "$1" |
	 sort | uniq -c | sed -e '/^[ 	]*1[ 	]/d')" || {
	echo >&2 Duplicate Signed-off-by lines.
	exit 1
}

```
</file>

### Arquivo: `.git/hooks/fsmonitor-watchman.sample`
<file path=".git/hooks/fsmonitor-watchman.sample" lines="174">
```sample
#!/usr/bin/perl

use strict;
use warnings;
use IPC::Open2;

# An example hook script to integrate Watchman
# (https://facebook.github.io/watchman/) with git to speed up detecting
# new and modified files.
#
# The hook is passed a version (currently 2) and last update token
# formatted as a string and outputs to stdout a new update token and
# all files that have been modified since the update token. Paths must
# be relative to the root of the working tree and separated by a single NUL.
#
# To enable this hook, rename this file to "query-watchman" and set
# 'git config core.fsmonitor .git/hooks/query-watchman'
#
my ($version, $last_update_token) = @ARGV;

# Uncomment for debugging
# print STDERR "$0 $version $last_update_token\n";

# Check the hook interface version
if ($version ne 2) {
	die "Unsupported query-fsmonitor hook version '$version'.\n" .
	    "Falling back to scanning...\n";
}

my $git_work_tree = get_working_dir();

my $retry = 1;

my $json_pkg;
eval {
	require JSON::XS;
	$json_pkg = "JSON::XS";
	1;
} or do {
	require JSON::PP;
	$json_pkg = "JSON::PP";
};

launch_watchman();

sub launch_watchman {
	my $o = watchman_query();
	if (is_work_tree_watched($o)) {
		output_result($o->{clock}, @{$o->{files}});
	}
}

sub output_result {
	my ($clockid, @files) = @_;

	# Uncomment for debugging watchman output
	# open (my $fh, ">", ".git/watchman-output.out");
	# binmode $fh, ":utf8";
	# print $fh "$clockid\n@files\n";
	# close $fh;

	binmode STDOUT, ":utf8";
	print $clockid;
	print "\0";
	local $, = "\0";
	print @files;
}

sub watchman_clock {
	my $response = qx/watchman clock "$git_work_tree"/;
	die "Failed to get clock id on '$git_work_tree'.\n" .
		"Falling back to scanning...\n" if $? != 0;

	return $json_pkg->new->utf8->decode($response);
}

sub watchman_query {
	my $pid = open2(\*CHLD_OUT, \*CHLD_IN, 'watchman -j --no-pretty')
	or die "open2() failed: $!\n" .
	"Falling back to scanning...\n";

	# In the query expression below we're asking for names of files that
	# changed since $last_update_token but not from the .git folder.
	#
	# To accomplish this, we're using the "since" generator to use the
	# recency index to select candidate nodes and "fields" to limit the
	# output to file names only. Then we're using the "expression" term to
	# further constrain the results.
	my $last_update_line = "";
	if (substr($last_update_token, 0, 1) eq "c") {
		$last_update_token = "\"$last_update_token\"";
		$last_update_line = qq[\n"since": $last_update_token,];
	}
	my $query = <<"	END";
		["query", "$git_work_tree", {$last_update_line
			"fields": ["name"],
			"expression": ["not", ["dirname", ".git"]]
		}]
	END

	# Uncomment for debugging the watchman query
	# open (my $fh, ">", ".git/watchman-query.json");
	# print $fh $query;
	# close $fh;

	print CHLD_IN $query;
	close CHLD_IN;
	my $response = do {local $/; <CHLD_OUT>};

	# Uncomment for debugging the watch response
	# open ($fh, ">", ".git/watchman-response.json");
	# print $fh $response;
	# close $fh;

	die "Watchman: command returned no output.\n" .
	"Falling back to scanning...\n" if $response eq "";
	die "Watchman: command returned invalid output: $response\n" .
	"Falling back to scanning...\n" unless $response =~ /^\{/;

	return $json_pkg->new->utf8->decode($response);
}

sub is_work_tree_watched {
	my ($output) = @_;
	my $error = $output->{error};
	if ($retry > 0 and $error and $error =~ m/unable to resolve root .* directory (.*) is not watched/) {
		$retry--;
		my $response = qx/watchman watch "$git_work_tree"/;
		die "Failed to make watchman watch '$git_work_tree'.\n" .
		    "Falling back to scanning...\n" if $? != 0;
		$output = $json_pkg->new->utf8->decode($response);
		$error = $output->{error};
		die "Watchman: $error.\n" .
		"Falling back to scanning...\n" if $error;

		# Uncomment for debugging watchman output
		# open (my $fh, ">", ".git/watchman-output.out");
		# close $fh;

		# Watchman will always return all files on the first query so
		# return the fast "everything is dirty" flag to git and do the
		# Watchman query just to get it over with now so we won't pay
		# the cost in git to look up each individual file.
		my $o = watchman_clock();
		$error = $output->{error};

		die "Watchman: $error.\n" .
		"Falling back to scanning...\n" if $error;

		output_result($o->{clock}, ("/"));
		$last_update_token = $o->{clock};

		eval { launch_watchman() };
		return 0;
	}

	die "Watchman: $error.\n" .
	"Falling back to scanning...\n" if $error;

	return 1;
}

sub get_working_dir {
	my $working_dir;
	if ($^O =~ 'msys' || $^O =~ 'cygwin') {
		$working_dir = Win32::GetCwd();
		$working_dir =~ tr/\\/\//;
	} else {
		require Cwd;
		$working_dir = Cwd::cwd();
	}

	return $working_dir;
}

```
</file>

### Arquivo: `.git/hooks/post-update.sample`
<file path=".git/hooks/post-update.sample" lines="8">
```sample
#!/bin/sh
#
# An example hook script to prepare a packed repository for use over
# dumb transports.
#
# To enable this hook, rename this file to "post-update".

exec git update-server-info

```
</file>

### Arquivo: `.git/hooks/pre-applypatch.sample`
<file path=".git/hooks/pre-applypatch.sample" lines="14">
```sample
#!/bin/sh
#
# An example hook script to verify what is about to be committed
# by applypatch from an e-mail message.
#
# The hook should exit with non-zero status after issuing an
# appropriate message if it wants to stop the commit.
#
# To enable this hook, rename this file to "pre-applypatch".

. git-sh-setup
precommit="$(git rev-parse --git-path hooks/pre-commit)"
test -x "$precommit" && exec "$precommit" ${1+"$@"}
:

```
</file>

### Arquivo: `.git/hooks/pre-commit.sample`
<file path=".git/hooks/pre-commit.sample" lines="49">
```sample
#!/bin/sh
#
# An example hook script to verify what is about to be committed.
# Called by "git commit" with no arguments.  The hook should
# exit with non-zero status after issuing an appropriate message if
# it wants to stop the commit.
#
# To enable this hook, rename this file to "pre-commit".

if git rev-parse --verify HEAD >/dev/null 2>&1
then
	against=HEAD
else
	# Initial commit: diff against an empty tree object
	against=$(git hash-object -t tree /dev/null)
fi

# If you want to allow non-ASCII filenames set this variable to true.
allownonascii=$(git config --type=bool hooks.allownonascii)

# Redirect output to stderr.
exec 1>&2

# Cross platform projects tend to avoid non-ASCII filenames; prevent
# them from being added to the repository. We exploit the fact that the
# printable range starts at the space character and ends with tilde.
if [ "$allownonascii" != "true" ] &&
	# Note that the use of brackets around a tr range is ok here, (it's
	# even required, for portability to Solaris 10's /usr/bin/tr), since
	# the square bracket bytes happen to fall in the designated range.
	test $(git diff-index --cached --name-only --diff-filter=A -z $against |
	  LC_ALL=C tr -d '[ -~]\0' | wc -c) != 0
then
	cat <<\EOF
Error: Attempt to add a non-ASCII file name.

This can cause problems if you want to work with people on other platforms.

To be portable it is advisable to rename the file.

If you know what you are doing you can disable this check using:

  git config hooks.allownonascii true
EOF
	exit 1
fi

# If there are whitespace errors, print the offending file names and fail.
exec git diff-index --check --cached $against --

```
</file>

### Arquivo: `.git/hooks/pre-merge-commit.sample`
<file path=".git/hooks/pre-merge-commit.sample" lines="13">
```sample
#!/bin/sh
#
# An example hook script to verify what is about to be committed.
# Called by "git merge" with no arguments.  The hook should
# exit with non-zero status after issuing an appropriate message to
# stderr if it wants to stop the merge commit.
#
# To enable this hook, rename this file to "pre-merge-commit".

. git-sh-setup
test -x "$GIT_DIR/hooks/pre-commit" &&
        exec "$GIT_DIR/hooks/pre-commit"
:

```
</file>

### Arquivo: `.git/hooks/pre-push.sample`
<file path=".git/hooks/pre-push.sample" lines="53">
```sample
#!/bin/sh

# An example hook script to verify what is about to be pushed.  Called by "git
# push" after it has checked the remote status, but before anything has been
# pushed.  If this script exits with a non-zero status nothing will be pushed.
#
# This hook is called with the following parameters:
#
# $1 -- Name of the remote to which the push is being done
# $2 -- URL to which the push is being done
#
# If pushing without using a named remote those arguments will be equal.
#
# Information about the commits which are being pushed is supplied as lines to
# the standard input in the form:
#
#   <local ref> <local oid> <remote ref> <remote oid>
#
# This sample shows how to prevent push of commits where the log message starts
# with "WIP" (work in progress).

remote="$1"
url="$2"

zero=$(git hash-object --stdin </dev/null | tr '[0-9a-f]' '0')

while read local_ref local_oid remote_ref remote_oid
do
	if test "$local_oid" = "$zero"
	then
		# Handle delete
		:
	else
		if test "$remote_oid" = "$zero"
		then
			# New branch, examine all commits
			range="$local_oid"
		else
			# Update to existing branch, examine new commits
			range="$remote_oid..$local_oid"
		fi

		# Check for WIP commit
		commit=$(git rev-list -n 1 --grep '^WIP' "$range")
		if test -n "$commit"
		then
			echo >&2 "Found WIP commit in $local_ref, not pushing"
			exit 1
		fi
	fi
done

exit 0

```
</file>

### Arquivo: `.git/hooks/pre-rebase.sample`
<file path=".git/hooks/pre-rebase.sample" lines="169">
```sample
#!/bin/sh
#
# Copyright (c) 2006, 2008 Junio C Hamano
#
# The "pre-rebase" hook is run just before "git rebase" starts doing
# its job, and can prevent the command from running by exiting with
# non-zero status.
#
# The hook is called with the following parameters:
#
# $1 -- the upstream the series was forked from.
# $2 -- the branch being rebased (or empty when rebasing the current branch).
#
# This sample shows how to prevent topic branches that are already
# merged to 'next' branch from getting rebased, because allowing it
# would result in rebasing already published history.

publish=next
basebranch="$1"
if test "$#" = 2
then
	topic="refs/heads/$2"
else
	topic=`git symbolic-ref HEAD` ||
	exit 0 ;# we do not interrupt rebasing detached HEAD
fi

case "$topic" in
refs/heads/??/*)
	;;
*)
	exit 0 ;# we do not interrupt others.
	;;
esac

# Now we are dealing with a topic branch being rebased
# on top of master.  Is it OK to rebase it?

# Does the topic really exist?
git show-ref -q "$topic" || {
	echo >&2 "No such branch $topic"
	exit 1
}

# Is topic fully merged to master?
not_in_master=`git rev-list --pretty=oneline ^master "$topic"`
if test -z "$not_in_master"
then
	echo >&2 "$topic is fully merged to master; better remove it."
	exit 1 ;# we could allow it, but there is no point.
fi

# Is topic ever merged to next?  If so you should not be rebasing it.
only_next_1=`git rev-list ^master "^$topic" ${publish} | sort`
only_next_2=`git rev-list ^master           ${publish} | sort`
if test "$only_next_1" = "$only_next_2"
then
	not_in_topic=`git rev-list "^$topic" master`
	if test -z "$not_in_topic"
	then
		echo >&2 "$topic is already up to date with master"
		exit 1 ;# we could allow it, but there is no point.
	else
		exit 0
	fi
else
	not_in_next=`git rev-list --pretty=oneline ^${publish} "$topic"`
	/usr/bin/perl -e '
		my $topic = $ARGV[0];
		my $msg = "* $topic has commits already merged to public branch:\n";
		my (%not_in_next) = map {
			/^([0-9a-f]+) /;
			($1 => 1);
		} split(/\n/, $ARGV[1]);
		for my $elem (map {
				/^([0-9a-f]+) (.*)$/;
				[$1 => $2];
			} split(/\n/, $ARGV[2])) {
			if (!exists $not_in_next{$elem->[0]}) {
				if ($msg) {
					print STDERR $msg;
					undef $msg;
				}
				print STDERR " $elem->[1]\n";
			}
		}
	' "$topic" "$not_in_next" "$not_in_master"
	exit 1
fi

<<\DOC_END

This sample hook safeguards topic branches that have been
published from being rewound.

The workflow assumed here is:

 * Once a topic branch forks from "master", "master" is never
   merged into it again (either directly or indirectly).

 * Once a topic branch is fully cooked and merged into "master",
   it is deleted.  If you need to build on top of it to correct
   earlier mistakes, a new topic branch is created by forking at
   the tip of the "master".  This is not strictly necessary, but
   it makes it easier to keep your history simple.

 * Whenever you need to test or publish your changes to topic
   branches, merge them into "next" branch.

The script, being an example, hardcodes the publish branch name
to be "next", but it is trivial to make it configurable via
$GIT_DIR/config mechanism.

With this workflow, you would want to know:

(1) ... if a topic branch has ever been merged to "next".  Young
    topic branches can have stupid mistakes you would rather
    clean up before publishing, and things that have not been
    merged into other branches can be easily rebased without
    affecting other people.  But once it is published, you would
    not want to rewind it.

(2) ... if a topic branch has been fully merged to "master".
    Then you can delete it.  More importantly, you should not
    build on top of it -- other people may already want to
    change things related to the topic as patches against your
    "master", so if you need further changes, it is better to
    fork the topic (perhaps with the same name) afresh from the
    tip of "master".

Let's look at this example:

		   o---o---o---o---o---o---o---o---o---o "next"
		  /       /           /           /
		 /   a---a---b A     /           /
		/   /               /           /
	       /   /   c---c---c---c B         /
	      /   /   /             \         /
	     /   /   /   b---b C     \       /
	    /   /   /   /             \     /
    ---o---o---o---o---o---o---o---o---o---o---o "master"


A, B and C are topic branches.

 * A has one fix since it was merged up to "next".

 * B has finished.  It has been fully merged up to "master" and "next",
   and is ready to be deleted.

 * C has not merged to "next" at all.

We would want to allow C to be rebased, refuse A, and encourage
B to be deleted.

To compute (1):

	git rev-list ^master ^topic next
	git rev-list ^master        next

	if these match, topic has not merged in next at all.

To compute (2):

	git rev-list master..topic

	if this is empty, it is fully merged to "master".

DOC_END

```
</file>

### Arquivo: `.git/hooks/pre-receive.sample`
<file path=".git/hooks/pre-receive.sample" lines="24">
```sample
#!/bin/sh
#
# An example hook script to make use of push options.
# The example simply echoes all push options that start with 'echoback='
# and rejects all pushes when the "reject" push option is used.
#
# To enable this hook, rename this file to "pre-receive".

if test -n "$GIT_PUSH_OPTION_COUNT"
then
	i=0
	while test "$i" -lt "$GIT_PUSH_OPTION_COUNT"
	do
		eval "value=\$GIT_PUSH_OPTION_$i"
		case "$value" in
		echoback=*)
			echo "echo from the pre-receive-hook: ${value#*=}" >&2
			;;
		reject)
			exit 1
		esac
		i=$((i + 1))
	done
fi

```
</file>

### Arquivo: `.git/hooks/prepare-commit-msg.sample`
<file path=".git/hooks/prepare-commit-msg.sample" lines="42">
```sample
#!/bin/sh
#
# An example hook script to prepare the commit log message.
# Called by "git commit" with the name of the file that has the
# commit message, followed by the description of the commit
# message's source.  The hook's purpose is to edit the commit
# message file.  If the hook fails with a non-zero status,
# the commit is aborted.
#
# To enable this hook, rename this file to "prepare-commit-msg".

# This hook includes three examples. The first one removes the
# "# Please enter the commit message..." help message.
#
# The second includes the output of "git diff --name-status -r"
# into the message, just before the "git status" output.  It is
# commented because it doesn't cope with --amend or with squashed
# commits.
#
# The third example adds a Signed-off-by line to the message, that can
# still be edited.  This is rarely a good idea.

COMMIT_MSG_FILE=$1
COMMIT_SOURCE=$2
SHA1=$3

/usr/bin/perl -i.bak -ne 'print unless(m/^. Please enter the commit message/..m/^#$/)' "$COMMIT_MSG_FILE"

# case "$COMMIT_SOURCE,$SHA1" in
#  ,|template,)
#    /usr/bin/perl -i.bak -pe '
#       print "\n" . `git diff --cached --name-status -r`
# 	 if /^#/ && $first++ == 0' "$COMMIT_MSG_FILE" ;;
#  *) ;;
# esac

# SOB=$(git var GIT_COMMITTER_IDENT | sed -n 's/^\(.*>\).*$/Signed-off-by: \1/p')
# git interpret-trailers --in-place --trailer "$SOB" "$COMMIT_MSG_FILE"
# if test -z "$COMMIT_SOURCE"
# then
#   /usr/bin/perl -i.bak -pe 'print "\n" if !$first_line++' "$COMMIT_MSG_FILE"
# fi

```
</file>

### Arquivo: `.git/hooks/push-to-checkout.sample`
<file path=".git/hooks/push-to-checkout.sample" lines="78">
```sample
#!/bin/sh

# An example hook script to update a checked-out tree on a git push.
#
# This hook is invoked by git-receive-pack(1) when it reacts to git
# push and updates reference(s) in its repository, and when the push
# tries to update the branch that is currently checked out and the
# receive.denyCurrentBranch configuration variable is set to
# updateInstead.
#
# By default, such a push is refused if the working tree and the index
# of the remote repository has any difference from the currently
# checked out commit; when both the working tree and the index match
# the current commit, they are updated to match the newly pushed tip
# of the branch. This hook is to be used to override the default
# behaviour; however the code below reimplements the default behaviour
# as a starting point for convenient modification.
#
# The hook receives the commit with which the tip of the current
# branch is going to be updated:
commit=$1

# It can exit with a non-zero status to refuse the push (when it does
# so, it must not modify the index or the working tree).
die () {
	echo >&2 "$*"
	exit 1
}

# Or it can make any necessary changes to the working tree and to the
# index to bring them to the desired state when the tip of the current
# branch is updated to the new commit, and exit with a zero status.
#
# For example, the hook can simply run git read-tree -u -m HEAD "$1"
# in order to emulate git fetch that is run in the reverse direction
# with git push, as the two-tree form of git read-tree -u -m is
# essentially the same as git switch or git checkout that switches
# branches while keeping the local changes in the working tree that do
# not interfere with the difference between the branches.

# The below is a more-or-less exact translation to shell of the C code
# for the default behaviour for git's push-to-checkout hook defined in
# the push_to_deploy() function in builtin/receive-pack.c.
#
# Note that the hook will be executed from the repository directory,
# not from the working tree, so if you want to perform operations on
# the working tree, you will have to adapt your code accordingly, e.g.
# by adding "cd .." or using relative paths.

if ! git update-index -q --ignore-submodules --refresh
then
	die "Up-to-date check failed"
fi

if ! git diff-files --quiet --ignore-submodules --
then
	die "Working directory has unstaged changes"
fi

# This is a rough translation of:
#
#   head_has_history() ? "HEAD" : EMPTY_TREE_SHA1_HEX
if git cat-file -e HEAD 2>/dev/null
then
	head=HEAD
else
	head=$(git hash-object -t tree --stdin </dev/null)
fi

if ! git diff-index --quiet --cached --ignore-submodules $head --
then
	die "Working directory has staged changes"
fi

if ! git read-tree -u -m "$commit"
then
	die "Could not update working tree to new HEAD"
fi

```
</file>

### Arquivo: `.git/hooks/sendemail-validate.sample`
<file path=".git/hooks/sendemail-validate.sample" lines="77">
```sample
#!/bin/sh

# An example hook script to validate a patch (and/or patch series) before
# sending it via email.
#
# The hook should exit with non-zero status after issuing an appropriate
# message if it wants to prevent the email(s) from being sent.
#
# To enable this hook, rename this file to "sendemail-validate".
#
# By default, it will only check that the patch(es) can be applied on top of
# the default upstream branch without conflicts in a secondary worktree. After
# validation (successful or not) of the last patch of a series, the worktree
# will be deleted.
#
# The following config variables can be set to change the default remote and
# remote ref that are used to apply the patches against:
#
#   sendemail.validateRemote (default: origin)
#   sendemail.validateRemoteRef (default: HEAD)
#
# Replace the TODO placeholders with appropriate checks according to your
# needs.

validate_cover_letter () {
	file="$1"
	# TODO: Replace with appropriate checks (e.g. spell checking).
	true
}

validate_patch () {
	file="$1"
	# Ensure that the patch applies without conflicts.
	git am -3 "$file" || return
	# TODO: Replace with appropriate checks for this patch
	# (e.g. checkpatch.pl).
	true
}

validate_series () {
	# TODO: Replace with appropriate checks for the whole series
	# (e.g. quick build, coding style checks, etc.).
	true
}

# main -------------------------------------------------------------------------

if test "$GIT_SENDEMAIL_FILE_COUNTER" = 1
then
	remote=$(git config --default origin --get sendemail.validateRemote) &&
	ref=$(git config --default HEAD --get sendemail.validateRemoteRef) &&
	worktree=$(mktemp --tmpdir -d sendemail-validate.XXXXXXX) &&
	git worktree add -fd --checkout "$worktree" "refs/remotes/$remote/$ref" &&
	git config --replace-all sendemail.validateWorktree "$worktree"
else
	worktree=$(git config --get sendemail.validateWorktree)
fi || {
	echo "sendemail-validate: error: failed to prepare worktree" >&2
	exit 1
}

unset GIT_DIR GIT_WORK_TREE
cd "$worktree" &&

if grep -q "^diff --git " "$1"
then
	validate_patch "$1"
else
	validate_cover_letter "$1"
fi &&

if test "$GIT_SENDEMAIL_FILE_COUNTER" = "$GIT_SENDEMAIL_FILE_TOTAL"
then
	git config --unset-all sendemail.validateWorktree &&
	trap 'git worktree remove -ff "$worktree"' EXIT &&
	validate_series
fi

```
</file>

### Arquivo: `.git/hooks/update.sample`
<file path=".git/hooks/update.sample" lines="128">
```sample
#!/bin/sh
#
# An example hook script to block unannotated tags from entering.
# Called by "git receive-pack" with arguments: refname sha1-old sha1-new
#
# To enable this hook, rename this file to "update".
#
# Config
# ------
# hooks.allowunannotated
#   This boolean sets whether unannotated tags will be allowed into the
#   repository.  By default they won't be.
# hooks.allowdeletetag
#   This boolean sets whether deleting tags will be allowed in the
#   repository.  By default they won't be.
# hooks.allowmodifytag
#   This boolean sets whether a tag may be modified after creation. By default
#   it won't be.
# hooks.allowdeletebranch
#   This boolean sets whether deleting branches will be allowed in the
#   repository.  By default they won't be.
# hooks.denycreatebranch
#   This boolean sets whether remotely creating branches will be denied
#   in the repository.  By default this is allowed.
#

# --- Command line
refname="$1"
oldrev="$2"
newrev="$3"

# --- Safety check
if [ -z "$GIT_DIR" ]; then
	echo "Don't run this script from the command line." >&2
	echo " (if you want, you could supply GIT_DIR then run" >&2
	echo "  $0 <ref> <oldrev> <newrev>)" >&2
	exit 1
fi

if [ -z "$refname" -o -z "$oldrev" -o -z "$newrev" ]; then
	echo "usage: $0 <ref> <oldrev> <newrev>" >&2
	exit 1
fi

# --- Config
allowunannotated=$(git config --type=bool hooks.allowunannotated)
allowdeletebranch=$(git config --type=bool hooks.allowdeletebranch)
denycreatebranch=$(git config --type=bool hooks.denycreatebranch)
allowdeletetag=$(git config --type=bool hooks.allowdeletetag)
allowmodifytag=$(git config --type=bool hooks.allowmodifytag)

# check for no description
projectdesc=$(sed -e '1q' "$GIT_DIR/description")
case "$projectdesc" in
"Unnamed repository"* | "")
	echo "*** Project description file hasn't been set" >&2
	exit 1
	;;
esac

# --- Check types
# if $newrev is 0000...0000, it's a commit to delete a ref.
zero=$(git hash-object --stdin </dev/null | tr '[0-9a-f]' '0')
if [ "$newrev" = "$zero" ]; then
	newrev_type=delete
else
	newrev_type=$(git cat-file -t $newrev)
fi

case "$refname","$newrev_type" in
	refs/tags/*,commit)
		# un-annotated tag
		short_refname=${refname##refs/tags/}
		if [ "$allowunannotated" != "true" ]; then
			echo "*** The un-annotated tag, $short_refname, is not allowed in this repository" >&2
			echo "*** Use 'git tag [ -a | -s ]' for tags you want to propagate." >&2
			exit 1
		fi
		;;
	refs/tags/*,delete)
		# delete tag
		if [ "$allowdeletetag" != "true" ]; then
			echo "*** Deleting a tag is not allowed in this repository" >&2
			exit 1
		fi
		;;
	refs/tags/*,tag)
		# annotated tag
		if [ "$allowmodifytag" != "true" ] && git rev-parse $refname > /dev/null 2>&1
		then
			echo "*** Tag '$refname' already exists." >&2
			echo "*** Modifying a tag is not allowed in this repository." >&2
			exit 1
		fi
		;;
	refs/heads/*,commit)
		# branch
		if [ "$oldrev" = "$zero" -a "$denycreatebranch" = "true" ]; then
			echo "*** Creating a branch is not allowed in this repository" >&2
			exit 1
		fi
		;;
	refs/heads/*,delete)
		# delete branch
		if [ "$allowdeletebranch" != "true" ]; then
			echo "*** Deleting a branch is not allowed in this repository" >&2
			exit 1
		fi
		;;
	refs/remotes/*,commit)
		# tracking branch
		;;
	refs/remotes/*,delete)
		# delete tracking branch
		if [ "$allowdeletebranch" != "true" ]; then
			echo "*** Deleting a tracking branch is not allowed in this repository" >&2
			exit 1
		fi
		;;
	*)
		# Anything else (is there anything else?)
		echo "*** Update hook: unknown type of update to ref $refname of type $newrev_type" >&2
		exit 1
		;;
esac

# --- Finished
exit 0

```
</file>

### Arquivo: `.git/info/exclude`
<file path=".git/info/exclude" lines="6">
```
# git ls-files --others --exclude-from=.git/info/exclude
# Lines that start with '#' are comments.
# For a project mostly in C, the following would be a good set of
# exclude patterns (uncomment them if you want to use them):
# *.[oa]
# *~

```
</file>

### Arquivo: `.git/logs/HEAD`
<file path=".git/logs/HEAD" lines="13">
```
0000000000000000000000000000000000000000 e540d799fc0bf7f248e41150d7cbb181e728ea85 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1774587158 -0300	commit (initial): 26-03
e540d799fc0bf7f248e41150d7cbb181e728ea85 255392d93c88e58ea50d6acdf2ada23fa374d277 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1774619890 -0300	commit: links sociais adicionados
255392d93c88e58ea50d6acdf2ada23fa374d277 5261aeca86f46b0438c1c0aeaf6a60cc38597f2c Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1774734058 -0300	commit: 28-03
5261aeca86f46b0438c1c0aeaf6a60cc38597f2c 04fb1753c0ce09bacfd3d63bd41ebe95dda29931 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1774893656 -0300	commit: 30/03
04fb1753c0ce09bacfd3d63bd41ebe95dda29931 737503dc934c4947656aa8aaa1b6da460b889d3d Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1775091608 -0300	commit: 04-01
737503dc934c4947656aa8aaa1b6da460b889d3d 57f229201a44ee6f7745c51f1f2610e7c254fc01 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1775163972 -0300	commit: add fullmetal
57f229201a44ee6f7745c51f1f2610e7c254fc01 c6edaca68bdac96470c758357ecd15a8b48b73ea Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1775189200 -0300	commit: fullmetal corrigido
c6edaca68bdac96470c758357ecd15a8b48b73ea 21207c7833beb663839474f3e03485ab331472d3 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1775189637 -0300	commit: tofukashi
21207c7833beb663839474f3e03485ab331472d3 b2767fdb07e7d51eeba990a384dcde4a1a8486da Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1775190168 -0300	commit: 0402
b2767fdb07e7d51eeba990a384dcde4a1a8486da 9e2b83b149f35c0241d96c1f24535f647f012916 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1775191349 -0300	commit: fma collectoin added
9e2b83b149f35c0241d96c1f24535f647f012916 3315f8df7eaca06c2a19655c7be4873ee565b7a2 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1775483841 -0300	commit: ore series added
3315f8df7eaca06c2a19655c7be4873ee565b7a2 51d71ad4d6b9903712b0837e770a6e06c92081cf Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1780963738 -0300	commit: marriagetoxinandaakanebanashi
51d71ad4d6b9903712b0837e770a6e06c92081cf 2865d6658fb520a7c52795d592d04b654bbaf67e Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1780963740 -0300	pull --tags origin main: Merge made by the 'ort' strategy.

```
</file>

### Arquivo: `.git/logs/refs/heads/main`
<file path=".git/logs/refs/heads/main" lines="13">
```
0000000000000000000000000000000000000000 e540d799fc0bf7f248e41150d7cbb181e728ea85 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1774587158 -0300	commit (initial): 26-03
e540d799fc0bf7f248e41150d7cbb181e728ea85 255392d93c88e58ea50d6acdf2ada23fa374d277 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1774619890 -0300	commit: links sociais adicionados
255392d93c88e58ea50d6acdf2ada23fa374d277 5261aeca86f46b0438c1c0aeaf6a60cc38597f2c Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1774734058 -0300	commit: 28-03
5261aeca86f46b0438c1c0aeaf6a60cc38597f2c 04fb1753c0ce09bacfd3d63bd41ebe95dda29931 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1774893656 -0300	commit: 30/03
04fb1753c0ce09bacfd3d63bd41ebe95dda29931 737503dc934c4947656aa8aaa1b6da460b889d3d Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1775091608 -0300	commit: 04-01
737503dc934c4947656aa8aaa1b6da460b889d3d 57f229201a44ee6f7745c51f1f2610e7c254fc01 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1775163972 -0300	commit: add fullmetal
57f229201a44ee6f7745c51f1f2610e7c254fc01 c6edaca68bdac96470c758357ecd15a8b48b73ea Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1775189200 -0300	commit: fullmetal corrigido
c6edaca68bdac96470c758357ecd15a8b48b73ea 21207c7833beb663839474f3e03485ab331472d3 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1775189637 -0300	commit: tofukashi
21207c7833beb663839474f3e03485ab331472d3 b2767fdb07e7d51eeba990a384dcde4a1a8486da Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1775190168 -0300	commit: 0402
b2767fdb07e7d51eeba990a384dcde4a1a8486da 9e2b83b149f35c0241d96c1f24535f647f012916 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1775191349 -0300	commit: fma collectoin added
9e2b83b149f35c0241d96c1f24535f647f012916 3315f8df7eaca06c2a19655c7be4873ee565b7a2 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1775483841 -0300	commit: ore series added
3315f8df7eaca06c2a19655c7be4873ee565b7a2 51d71ad4d6b9903712b0837e770a6e06c92081cf Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1780963738 -0300	commit: marriagetoxinandaakanebanashi
51d71ad4d6b9903712b0837e770a6e06c92081cf 2865d6658fb520a7c52795d592d04b654bbaf67e Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1780963740 -0300	pull --tags origin main: Merge made by the 'ort' strategy.

```
</file>

### Arquivo: `.git/logs/refs/remotes/origin/main`
<file path=".git/logs/refs/remotes/origin/main" lines="13">
```
0000000000000000000000000000000000000000 e540d799fc0bf7f248e41150d7cbb181e728ea85 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1774587196 -0300	update by push
e540d799fc0bf7f248e41150d7cbb181e728ea85 255392d93c88e58ea50d6acdf2ada23fa374d277 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1774619895 -0300	update by push
255392d93c88e58ea50d6acdf2ada23fa374d277 5261aeca86f46b0438c1c0aeaf6a60cc38597f2c Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1774734062 -0300	update by push
5261aeca86f46b0438c1c0aeaf6a60cc38597f2c 04fb1753c0ce09bacfd3d63bd41ebe95dda29931 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1774893661 -0300	update by push
04fb1753c0ce09bacfd3d63bd41ebe95dda29931 737503dc934c4947656aa8aaa1b6da460b889d3d Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1775091618 -0300	update by push
737503dc934c4947656aa8aaa1b6da460b889d3d 57f229201a44ee6f7745c51f1f2610e7c254fc01 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1775163976 -0300	update by push
57f229201a44ee6f7745c51f1f2610e7c254fc01 c6edaca68bdac96470c758357ecd15a8b48b73ea Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1775189208 -0300	update by push
c6edaca68bdac96470c758357ecd15a8b48b73ea 21207c7833beb663839474f3e03485ab331472d3 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1775189641 -0300	update by push
21207c7833beb663839474f3e03485ab331472d3 b2767fdb07e7d51eeba990a384dcde4a1a8486da Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1775190172 -0300	update by push
b2767fdb07e7d51eeba990a384dcde4a1a8486da 9e2b83b149f35c0241d96c1f24535f647f012916 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1775191353 -0300	update by push
9e2b83b149f35c0241d96c1f24535f647f012916 3315f8df7eaca06c2a19655c7be4873ee565b7a2 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1775483845 -0300	update by push
3315f8df7eaca06c2a19655c7be4873ee565b7a2 a383d8704c3923e46d397170b0b9c5be40a0a1b5 Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1780963740 -0300	pull --tags origin main: fast-forward
a383d8704c3923e46d397170b0b9c5be40a0a1b5 2865d6658fb520a7c52795d592d04b654bbaf67e Rhyan <lucas.rhyan@aluno.ifsertao-pe.edu.br> 1780963743 -0300	update by push

```
</file>

### Arquivo: `.git/objects/00/bea410118aa466bb0069f8cb17f6ba96026054`
<file path=".git/objects/00/bea410118aa466bb0069f8cb17f6ba96026054" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xed in position 2: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/02/b0da16663c5045341d3681c52d5bcee91fac6c`
<file path=".git/objects/02/b0da16663c5045341d3681c52d5bcee91fac6c" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xd5 in position 2: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/04/fb1753c0ce09bacfd3d63bd41ebe95dda29931`
<file path=".git/objects/04/fb1753c0ce09bacfd3d63bd41ebe95dda29931" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xa5 in position 2: invalid start byte>
```
</file>

### Arquivo: `.git/objects/0d/16df1c58b1d824bcf405627f0e7b7c12dd87de`
<file path=".git/objects/0d/16df1c58b1d824bcf405627f0e7b7c12dd87de" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xdd in position 2: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/0d/5ba7216595e32ef3d834788467800ccc6a3377`
<file path=".git/objects/0d/5ba7216595e32ef3d834788467800ccc6a3377" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xb6 in position 8: invalid start byte>
```
</file>

### Arquivo: `.git/objects/0f/6c580aa9791e8f000f6e6abcd8f4b7859134b3`
<file path=".git/objects/0f/6c580aa9791e8f000f6e6abcd8f4b7859134b3" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xc8 in position 17: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/1e/4c569ab13b4ad885304093ee2c6eb0a05d1fa8`
<file path=".git/objects/1e/4c569ab13b4ad885304093ee2c6eb0a05d1fa8" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xed in position 2: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/21/207c7833beb663839474f3e03485ab331472d3`
<file path=".git/objects/21/207c7833beb663839474f3e03485ab331472d3" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xa5 in position 2: invalid start byte>
```
</file>

### Arquivo: `.git/objects/25/4c7ee0814999814e3094dcf9d9d89fa4cfae50`
<file path=".git/objects/25/4c7ee0814999814e3094dcf9d9d89fa4cfae50" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode bytes in position 2-3: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/25/5392d93c88e58ea50d6acdf2ada23fa374d277`
<file path=".git/objects/25/5392d93c88e58ea50d6acdf2ada23fa374d277" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xa5 in position 2: invalid start byte>
```
</file>

### Arquivo: `.git/objects/26/a98f670727be7cebf83699bf572a37f56f1e75`
<file path=".git/objects/26/a98f670727be7cebf83699bf572a37f56f1e75" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xb6 in position 8: invalid start byte>
```
</file>

### Arquivo: `.git/objects/28/65d6658fb520a7c52795d592d04b654bbaf67e`
<file path=".git/objects/28/65d6658fb520a7c52795d592d04b654bbaf67e" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xa5 in position 2: invalid start byte>
```
</file>

### Arquivo: `.git/objects/28/9388cd964599bfcafc60363cdd120f79ffa07b`
<file path=".git/objects/28/9388cd964599bfcafc60363cdd120f79ffa07b" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xc8 in position 17: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/2c/da26733c2f376abf5e998570afcb918b7d205c`
<file path=".git/objects/2c/da26733c2f376abf5e998570afcb918b7d205c" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xc8 in position 17: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/2e/c0a027d3ea47c0620cf9536888aa47d2c4cd9e`
<file path=".git/objects/2e/c0a027d3ea47c0620cf9536888aa47d2c4cd9e" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xd5 in position 2: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/31/b6d326ee36d38d44a0e4d1837053a8a316a096`
<file path=".git/objects/31/b6d326ee36d38d44a0e4d1837053a8a316a096" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xd5 in position 2: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/33/15f8df7eaca06c2a19655c7be4873ee565b7a2`
<file path=".git/objects/33/15f8df7eaca06c2a19655c7be4873ee565b7a2" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xa5 in position 2: invalid start byte>
```
</file>

### Arquivo: `.git/objects/3a/132806fc3424d93dc0c878cdc38bdd878b6640`
<file path=".git/objects/3a/132806fc3424d93dc0c878cdc38bdd878b6640" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xb6 in position 8: invalid start byte>
```
</file>

### Arquivo: `.git/objects/43/90f96a5008728a9e329cc9d01b54f0d3d924d3`
<file path=".git/objects/43/90f96a5008728a9e329cc9d01b54f0d3d924d3" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xed in position 2: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/44/0d52ec278b3f2f82ad97cc387c46109d1b0962`
<file path=".git/objects/44/0d52ec278b3f2f82ad97cc387c46109d1b0962" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xb6 in position 8: invalid start byte>
```
</file>

### Arquivo: `.git/objects/51/d71ad4d6b9903712b0837e770a6e06c92081cf`
<file path=".git/objects/51/d71ad4d6b9903712b0837e770a6e06c92081cf" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xa5 in position 2: invalid start byte>
```
</file>

### Arquivo: `.git/objects/52/29ac79058d55669fdac8145efbc94a61564128`
<file path=".git/objects/52/29ac79058d55669fdac8145efbc94a61564128" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xb6 in position 8: invalid start byte>
```
</file>

### Arquivo: `.git/objects/52/61aeca86f46b0438c1c0aeaf6a60cc38597f2c`
<file path=".git/objects/52/61aeca86f46b0438c1c0aeaf6a60cc38597f2c" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xa5 in position 2: invalid start byte>
```
</file>

### Arquivo: `.git/objects/52/fbd19d52d5c69b30b7204044c0284b9e711563`
<file path=".git/objects/52/fbd19d52d5c69b30b7204044c0284b9e711563" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xb6 in position 8: invalid start byte>
```
</file>

### Arquivo: `.git/objects/57/f229201a44ee6f7745c51f1f2610e7c254fc01`
<file path=".git/objects/57/f229201a44ee6f7745c51f1f2610e7c254fc01" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xa5 in position 2: invalid start byte>
```
</file>

### Arquivo: `.git/objects/59/b3020ebb152870515f74966e013ae1e8988fbf`
<file path=".git/objects/59/b3020ebb152870515f74966e013ae1e8988fbf" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xd5 in position 2: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/61/96fc42ba24e0d8ee2fb0d7d5a5166068bd4a1f`
<file path=".git/objects/61/96fc42ba24e0d8ee2fb0d7d5a5166068bd4a1f" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode bytes in position 2-3: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/65/a112d20396d5c3bca771306e7b406f1ea1a324`
<file path=".git/objects/65/a112d20396d5c3bca771306e7b406f1ea1a324" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xc8 in position 17: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/66/aab072ae98d3b4591e7915b4cf11306702466c`
<file path=".git/objects/66/aab072ae98d3b4591e7915b4cf11306702466c" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xd6 in position 23: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/6a/1d7187e9ece2ec222fb4408c4a7239cb9a3686`
<file path=".git/objects/6a/1d7187e9ece2ec222fb4408c4a7239cb9a3686" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xb6 in position 8: invalid start byte>
```
</file>

### Arquivo: `.git/objects/6c/898533528d30a7d1288cd3575d3cfed2931603`
<file path=".git/objects/6c/898533528d30a7d1288cd3575d3cfed2931603" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xc8 in position 17: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/6f/8c28675684c3f9c94c9cd057364315ad4c11a3`
<file path=".git/objects/6f/8c28675684c3f9c94c9cd057364315ad4c11a3" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xb6 in position 8: invalid start byte>
```
</file>

### Arquivo: `.git/objects/73/7503dc934c4947656aa8aaa1b6da460b889d3d`
<file path=".git/objects/73/7503dc934c4947656aa8aaa1b6da460b889d3d" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xa5 in position 2: invalid start byte>
```
</file>

### Arquivo: `.git/objects/76/7c3d2115a7ecd6638602f4dd2dd7f0c62e2a95`
<file path=".git/objects/76/7c3d2115a7ecd6638602f4dd2dd7f0c62e2a95" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xb6 in position 8: invalid start byte>
```
</file>

### Arquivo: `.git/objects/77/a0e8069d9ec29c1b9931f8180583035d3017ad`
<file path=".git/objects/77/a0e8069d9ec29c1b9931f8180583035d3017ad" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xd5 in position 2: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/7c/bafab6e74326e56986b6936c2b1734e42c2bb2`
<file path=".git/objects/7c/bafab6e74326e56986b6936c2b1734e42c2bb2" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0x86 in position 22: invalid start byte>
```
</file>

### Arquivo: `.git/objects/83/5ec99fa5faf40b18f8314264b6af4229a5aa18`
<file path=".git/objects/83/5ec99fa5faf40b18f8314264b6af4229a5aa18" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xed in position 2: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/96/e35c718d616baaf1a883d62793ee6764e0adc4`
<file path=".git/objects/96/e35c718d616baaf1a883d62793ee6764e0adc4" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xc8 in position 17: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/96/fa6298f81c0df167f0c85cd18a5bb9013d5831`
<file path=".git/objects/96/fa6298f81c0df167f0c85cd18a5bb9013d5831" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xc8 in position 17: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/97/12ca43494ef2ccfbcda471d5170a606196eacb`
<file path=".git/objects/97/12ca43494ef2ccfbcda471d5170a606196eacb" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xd5 in position 2: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/9e/2b83b149f35c0241d96c1f24535f647f012916`
<file path=".git/objects/9e/2b83b149f35c0241d96c1f24535f647f012916" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xa5 in position 2: invalid start byte>
```
</file>

### Arquivo: `.git/objects/9f/32a34b5143eea97c8e45796f3e451721d15155`
<file path=".git/objects/9f/32a34b5143eea97c8e45796f3e451721d15155" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xb6 in position 8: invalid start byte>
```
</file>

### Arquivo: `.git/objects/a1/4322498bdfec7ec28602916a05f7f0b0601f56`
<file path=".git/objects/a1/4322498bdfec7ec28602916a05f7f0b0601f56" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xd7 in position 24: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/a3/83d8704c3923e46d397170b0b9c5be40a0a1b5`
<file path=".git/objects/a3/83d8704c3923e46d397170b0b9c5be40a0a1b5" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xa5 in position 2: invalid start byte>
```
</file>

### Arquivo: `.git/objects/a4/af1ba73a91917aa6295fb07d6cce494fdc8701`
<file path=".git/objects/a4/af1ba73a91917aa6295fb07d6cce494fdc8701" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xb6 in position 8: invalid start byte>
```
</file>

### Arquivo: `.git/objects/ad/725ad88b9c08761a534eb5cc7c251944561ead`
<file path=".git/objects/ad/725ad88b9c08761a534eb5cc7c251944561ead" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xd6 in position 23: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/ad/d486ec011d0424f920e14220907990132199be`
<file path=".git/objects/ad/d486ec011d0424f920e14220907990132199be" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode bytes in position 2-3: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/b2/767fdb07e7d51eeba990a384dcde4a1a8486da`
<file path=".git/objects/b2/767fdb07e7d51eeba990a384dcde4a1a8486da" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xa5 in position 2: invalid start byte>
```
</file>

### Arquivo: `.git/objects/b2/b604acd5fb361f096223462544cf655b8ebf20`
<file path=".git/objects/b2/b604acd5fb361f096223462544cf655b8ebf20" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xb6 in position 8: invalid start byte>
```
</file>

### Arquivo: `.git/objects/b7/6524d24385ed257619a866bde384297be94929`
<file path=".git/objects/b7/6524d24385ed257619a866bde384297be94929" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xb6 in position 8: invalid start byte>
```
</file>

### Arquivo: `.git/objects/bd/c3bcdd17e5e8c44143fd304ac1d90e6cf3582b`
<file path=".git/objects/bd/c3bcdd17e5e8c44143fd304ac1d90e6cf3582b" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xc8 in position 17: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/c3/04b916fb3a1ab8bee7ef76ca8d1f6c7f7ab615`
<file path=".git/objects/c3/04b916fb3a1ab8bee7ef76ca8d1f6c7f7ab615" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xd5 in position 2: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/c3/4e326c52065b44b23cc48da057b20865cee652`
<file path=".git/objects/c3/4e326c52065b44b23cc48da057b20865cee652" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xd5 in position 2: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/c6/edaca68bdac96470c758357ecd15a8b48b73ea`
<file path=".git/objects/c6/edaca68bdac96470c758357ecd15a8b48b73ea" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xa5 in position 2: invalid start byte>
```
</file>

### Arquivo: `.git/objects/c7/3329f650ebf9d9796be95d09a9b2f796107769`
<file path=".git/objects/c7/3329f650ebf9d9796be95d09a9b2f796107769" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xed in position 2: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/d6/930dca63edc0ba0323bbd5f50ea4c65925c0ac`
<file path=".git/objects/d6/930dca63edc0ba0323bbd5f50ea4c65925c0ac" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xb2 in position 8: invalid start byte>
```
</file>

### Arquivo: `.git/objects/dc/677fc7aa71afbbb3379061bfc2acd6ed74bd70`
<file path=".git/objects/dc/677fc7aa71afbbb3379061bfc2acd6ed74bd70" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xb6 in position 8: invalid start byte>
```
</file>

### Arquivo: `.git/objects/de/afcf2b255a141d0bdced59806a03132921ed07`
<file path=".git/objects/de/afcf2b255a141d0bdced59806a03132921ed07" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xd5 in position 2: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/de/c1ea33aade40ea675d39a4e975f7dd38f49146`
<file path=".git/objects/de/c1ea33aade40ea675d39a4e975f7dd38f49146" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xd5 in position 2: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/e5/40d799fc0bf7f248e41150d7cbb181e728ea85`
<file path=".git/objects/e5/40d799fc0bf7f248e41150d7cbb181e728ea85" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xa5 in position 2: invalid start byte>
```
</file>

### Arquivo: `.git/objects/ee/926deede46482220f4fda7c71413eb36f45896`
<file path=".git/objects/ee/926deede46482220f4fda7c71413eb36f45896" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xed in position 2: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/ef/0155f353c5913ef1749cb1fc724bb7dba2cb5b`
<file path=".git/objects/ef/0155f353c5913ef1749cb1fc724bb7dba2cb5b" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xdd in position 2: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/ef/1813e3f4af8be431d4ba39664a3db4a144db60`
<file path=".git/objects/ef/1813e3f4af8be431d4ba39664a3db4a144db60" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xb6 in position 8: invalid start byte>
```
</file>

### Arquivo: `.git/objects/fd/25cc702355c4adde5ab3f6bf1b41610f3ab39d`
<file path=".git/objects/fd/25cc702355c4adde5ab3f6bf1b41610f3ab39d" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xc8 in position 17: invalid continuation byte>
```
</file>

### Arquivo: `.git/objects/fd/b9624f6fab1687edf7068f6666f41960fb7d6a`
<file path=".git/objects/fd/b9624f6fab1687edf7068f6666f41960fb7d6a" lines="0">
```
<erro ao ler arquivo: 'utf-8' codec can't decode byte 0xb6 in position 8: invalid start byte>
```
</file>

### Arquivo: `.git/refs/heads/main`
<file path=".git/refs/heads/main" lines="1">
```
2865d6658fb520a7c52795d592d04b654bbaf67e

```
</file>

### Arquivo: `.git/refs/remotes/origin/main`
<file path=".git/refs/remotes/origin/main" lines="1">
```
2865d6658fb520a7c52795d592d04b654bbaf67e

```
</file>

### Arquivo: `series/144866.html`
<file path="series/144866.html" lines="68">
```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Série 144866 - Coleção Completa</title>
    <style>
        body { font-family: 'Segoe UI', Arial, sans-serif; background-color: #f3e5d8; color: #57310a; margin: 0; padding: 0; }
        header { background-color: #e07333; color: white; padding: 30px; text-align: center; box-shadow: 0 4px 6px rgba(0,0,0,0.1); }
        header h1 { margin: 0; font-size: 2.5em; }
        .back-btn { display: inline-block; margin-top: 15px; color: white; text-decoration: none; font-weight: bold; background: rgba(0,0,0,0.2); padding: 8px 16px; border-radius: 20px; }
        .container { max-width: 1200px; margin: 40px auto; padding: 0 20px; }
        .grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); gap: 30px; }
        .card { background: white; border: 2px solid #57310a; border-radius: 12px; padding: 15px; text-align: center; box-shadow: 4px 4px 0px #57310a; transition: transform 0.2s; }
        .card:hover { transform: translateY(-5px); }
        .card img { max-width: 100%; height: 260px; object-fit: contain; border-radius: 6px; }
        .card h3 { font-size: 1.1em; margin: 12px 0; min-height: 44px; }
        .btn { display: block; background-color: #28a745; color: white; text-decoration: none; padding: 10px; border-radius: 6px; font-weight: bold; transition: background 0.2s; }
        .btn:hover { background-color: #218838; }
        .footer { text-align: center; padding: 20px; color: #666; margin-top: 40px; }
    </style>
</head>
<body>
    <header>
        <h1>📚 Série 144866</h1>
        <p>Preços e links de afiliados atualizados para a sua estante!</p>
        <a href="index.html" class="back-btn">⬅️ Voltar para o Catálogo</a>
    </header>
    
    <div class="container">
        <div class="grid">
            <div class="card">
                <img src="https://m.media-amazon.com/images/I/91KMrqiIRfL._SY466_.jpg" alt="Volume 01">
                <h3>Volume 01</h3>
                <a href="https://www.amazon.com.br/gp/product/B0FSYN8JN6" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>
            <div class="card">
                <img src="https://m.media-amazon.com/images/I/91UbpqbUThL._SY466_.jpg" alt="Volume 02">
                <h3>Volume 02</h3>
                <a href="https://www.amazon.com.br/gp/product/B0FT1F4XPH" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>
            <div class="card">
                <img src="https://m.media-amazon.com/images/I/91q4Kawx7qL._SY466_.jpg" alt="Volume 03">
                <h3>Volume 03</h3>
                <a href="https://www.amazon.com.br/gp/product/B0FSYQPPLW" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>
            <div class="card">
                <img src="https://m.media-amazon.com/images/I/91QnDyp2SNL._SY466_.jpg" alt="Volume 04">
                <h3>Volume 04</h3>
                <a href="https://www.amazon.com.br/gp/product/B0FTMYYG4F" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>
            <div class="card">
                <img src="https://m.media-amazon.com/images/I/91Gn-8r-dLL._SY466_.jpg" alt="Volume 05">
                <h3>Volume 05</h3>
                <a href="https://www.amazon.com.br/gp/product/B0FZLHXZ6J" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>
            <div class="card">
                <img src="https://m.media-amazon.com/images/I/91HaWQ2RnpL._SY466_.jpg" alt="Volume 06">
                <h3>Volume 06</h3>
                <a href="https://www.amazon.com.br/gp/product/B0G6GBWSN1" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>
        </div>
    </div>
    <div class="footer">
        <p>© Mundo Mangá Promos - Links de Associados Amazon</p>
    </div>
</body>
</html>
```
</file>

### Arquivo: `series/199547.html`
<file path="series/199547.html" lines="131">
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Série - Mundo Mangá Promos</title>
    <style>
        :root {
            --primary: #F28C4A;
            --bg: #f4f4f9;
            --text: #333;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg);
            color: var(--text);
            margin: 0;
            padding: 0;
        }
        header {
            background-color: var(--primary);
            color: white;
            padding: 20px;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        .container {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 20px;
        }
        .card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: transform 0.2s;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 15px;
            text-align: center;
        }
        .card:hover {
            transform: translateY(-5px);
        }
        .card img {
            max-width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 8px;
            margin-bottom: 15px;
        }
        .card h3 {
            margin: 0 0 15px 0;
            font-size: 1.1rem;
            flex-grow: 1;
        }
        .btn {
            background-color: #28a745;
            color: white;
            text-decoration: none;
            padding: 10px 20px;
            border-radius: 8px;
            font-weight: bold;
            width: 100%;
            box-sizing: border-box;
            display: inline-block;
        }
        .btn:hover {
            background-color: #218838;
        }
        .footer {
            text-align: center;
            padding: 20px;
            color: #666;
            margin-top: 40px;
        }
    </style>
</head>
<body>
    <header>
        <h1>📚 Coleção Completa</h1>
        <p>Complete a sua estante com os melhores preços!</p>
    </header>
    
    <div class="container">
        <div class="grid">

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71vaLgT+0ML._SY425_.jpg" alt="Volume 01">
                <h3>Volume 01</h3>
                <a href="https://www.amazon.com.br/gp/product/6525915066" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71CjSJlOQpL._SY466_.jpg" alt="Volume 02">
                <h3>Volume 02</h3>
                <a href="https://www.amazon.com.br/gp/product/6525934230" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/618Z4E5Yi9L._SY466_.jpg" alt="Volume 03">
                <h3>Volume 03</h3>
                <a href="https://www.amazon.com.br/gp/product/6525932831" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61lgRcLSkPL._SY466_.jpg" alt="Volume 04">
                <h3>Volume 04</h3>
                <a href="https://www.amazon.com.br/gp/product/6525928257" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61DQ7zPZhIL._SY466_.jpg" alt="Volume 05">
                <h3>Volume 05</h3>
                <a href="https://www.amazon.com.br/gp/product/6525925525" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

        </div>
    </div>
    <div class="footer">
        <p>© Mundo Mangá Promos - Links de Associado Amazon</p>
    </div>
</body>
</html>

```
</file>

### Arquivo: `series/30001.html`
<file path="series/30001.html" lines="78">
```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Série 30001 - Coleção Completa</title>
    <style>
        body { font-family: 'Segoe UI', Arial, sans-serif; background-color: #f3e5d8; color: #57310a; margin: 0; padding: 0; }
        header { background-color: #e07333; color: white; padding: 30px; text-align: center; box-shadow: 0 4px 6px rgba(0,0,0,0.1); }
        header h1 { margin: 0; font-size: 2.5em; }
        .back-btn { display: inline-block; margin-top: 15px; color: white; text-decoration: none; font-weight: bold; background: rgba(0,0,0,0.2); padding: 8px 16px; border-radius: 20px; }
        .container { max-width: 1200px; margin: 40px auto; padding: 0 20px; }
        .grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); gap: 30px; }
        .card { background: white; border: 2px solid #57310a; border-radius: 12px; padding: 15px; text-align: center; box-shadow: 4px 4px 0px #57310a; transition: transform 0.2s; }
        .card:hover { transform: translateY(-5px); }
        .card img { max-width: 100%; height: 260px; object-fit: contain; border-radius: 6px; }
        .card h3 { font-size: 1.1em; margin: 12px 0; min-height: 44px; }
        .btn { display: block; background-color: #28a745; color: white; text-decoration: none; padding: 10px; border-radius: 6px; font-weight: bold; transition: background 0.2s; }
        .btn:hover { background-color: #218838; }
        .footer { text-align: center; padding: 20px; color: #666; margin-top: 40px; }
    </style>
</head>
<body>
    <header>
        <h1>📚 Série 30001</h1>
        <p>Preços e links de afiliados atualizados para a sua estante!</p>
        <a href="index.html" class="back-btn">⬅️ Voltar para o Catálogo</a>
    </header>
    
    <div class="container">
        <div class="grid">
            <div class="card">
                <img src="https://m.media-amazon.com/images/I/81VI6wwVzVL._SY425_.jpg" alt="Volume 1">
                <h3>Volume 1</h3>
                <a href="https://www.amazon.com.br/gp/product/8542627199" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>
            <div class="card">
                <img src="https://m.media-amazon.com/images/I/91ZoKQv5XDL._SY425_.jpg" alt="Volume 2">
                <h3>Volume 2</h3>
                <a href="https://www.amazon.com.br/gp/product/8542629361" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>
            <div class="card">
                <img src="https://m.media-amazon.com/images/I/91HA3WeQ+tL._SY425_.jpg" alt="Volume 3">
                <h3>Volume 3</h3>
                <a href="https://www.amazon.com.br/gp/product/8542630416" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>
            <div class="card">
                <img src="https://m.media-amazon.com/images/I/81PL5VLbg3L._SY425_.jpg" alt="Volume 4">
                <h3>Volume 4</h3>
                <a href="https://www.amazon.com.br/gp/product/6555121254" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>
            <div class="card">
                <img src="https://m.media-amazon.com/images/I/91aPWMI7Q0L._SY385_.jpg" alt="Volume 5">
                <h3>Volume 5</h3>
                <a href="https://www.amazon.com.br/gp/product/655512282X" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>
            <div class="card">
                <img src="https://m.media-amazon.com/images/I/81k-CoEvddL._SY425_.jpg" alt="Volume 7">
                <h3>Volume 7</h3>
                <a href="https://www.amazon.com.br/gp/product/6555125667" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>
            <div class="card">
                <img src="https://m.media-amazon.com/images/I/91d7uvUhgkL._SY425_.jpg" alt="Volume 8">
                <h3>Volume 8</h3>
                <a href="https://www.amazon.com.br/gp/product/6555128100" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>
            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61MzGL61x+L._SY425_.jpg" alt="Volume 9">
                <h3>Volume 9</h3>
                <a href="https://www.amazon.com.br/gp/product/6559600181" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>
        </div>
    </div>
    <div class="footer">
        <p>© Mundo Mangá Promos - Links de Associados Amazon</p>
    </div>
</body>
</html>
```
</file>

### Arquivo: `series/index.html`
<file path="series/index.html" lines="79">
```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Catálogo de Séries - Mundo Mangá</title>
    <style>
        body { font-family: 'Segoe UI', Arial, sans-serif; background-color: #f3e5d8; color: #57310a; margin: 0; padding: 0; }
        header { background-color: #57310a; color: white; padding: 40px; text-align: center; }
        header h1 { margin: 0; font-size: 2.5em; }
        .container { max-width: 1000px; margin: 40px auto; padding: 0 20px; }
        .lista-series { display: flex; flex-direction: column; gap: 16px; list-style: none; padding: 0; }
        .item-serie a { 
            display: flex; 
            align-items: center; 
            background: white; 
            border: 2px solid #57310a; 
            border-radius: 12px; 
            padding: 20px; 
            color: #57310a; 
            text-decoration: none; 
            font-size: 1.3em; 
            font-weight: bold;
            box-shadow: 4px 4px 0px #57310a;
            transition: all 0.2s;
        }
        .item-serie a:hover { transform: translateX(5px); background-color: #fffcf5; }
        .item-serie a::before { content: "📖"; margin-right: 15px; font-size: 1.2em; }
        .footer { text-align: center; padding: 20px; color: #666; margin-top: 60px; }
    </style>
</head>
<body>
    <header>
        <h1>📚 Catálogo de Coleções</h1>
        <p>Selecione uma obra para ver todos os volumes disponíveis</p>
    </header>
    
    <div class="container">
        <ul class="lista-series">
            <li class="item-serie">
                <a href="101517.html">Série ID 101517</a>
            </li>
            <li class="item-serie">
                <a href="111233.html">Série ID 111233</a>
            </li>
            <li class="item-serie">
                <a href="144866.html">Série ID 144866</a>
            </li>
            <li class="item-serie">
                <a href="199547.html">Série ID 199547</a>
            </li>
            <li class="item-serie">
                <a href="30001.html">Série ID 30001</a>
            </li>
            <li class="item-serie">
                <a href="30012.html">Série ID 30012</a>
            </li>
            <li class="item-serie">
                <a href="30025.html">Série ID 30025</a>
            </li>
            <li class="item-serie">
                <a href="30908.html">Soul Eater</a>
            </li>
            <li class="item-serie">
                <a href="74489.html">Série ID 74489</a>
            </li>
            <li class="item-serie">
                <a href="86635.html">Kaguya-sama wa Kokurasetai: Tensaitachi no Renai Zunousen</a>
            </li>
            <li class="item-serie">
                <a href="98235.html">Série ID 98235</a>
            </li>
        </ul>
    </div>
    <div class="footer">
        <p>Mundo Mangá Promos © 2026</p>
    </div>
</body>
</html>
```
</file>

### Arquivo: `series/101517/index.html`
<file path="series/101517/index.html" lines="221">
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Série - Mundo Mangá Promos</title>
    <style>
        :root {
            --primary: #F28C4A;
            --bg: #f4f4f9;
            --text: #333;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg);
            color: var(--text);
            margin: 0;
            padding: 0;
        }
        header {
            background-color: var(--primary);
            color: white;
            padding: 20px;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        .container {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 20px;
        }
        .card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: transform 0.2s;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 15px;
            text-align: center;
        }
        .card:hover {
            transform: translateY(-5px);
        }
        .card img {
            max-width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 8px;
            margin-bottom: 15px;
        }
        .card h3 {
            margin: 0 0 15px 0;
            font-size: 1.1rem;
            flex-grow: 1;
        }
        .btn {
            background-color: #28a745;
            color: white;
            text-decoration: none;
            padding: 10px 20px;
            border-radius: 8px;
            font-weight: bold;
            width: 100%;
            box-sizing: border-box;
            display: inline-block;
        }
        .btn:hover {
            background-color: #218838;
        }
        .footer {
            text-align: center;
            padding: 20px;
            color: #666;
            margin-top: 40px;
        }
    </style>
</head>
<body>
    <header>
        <h1>📚 Coleção Completa</h1>
        <p>Complete a sua estante com os melhores preços!</p>
    </header>
    
    <div class="container">
        <div class="grid">

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61ResbP4aPL._SY425_.jpg" alt="Volume 1">
                <h3>Volume 1</h3>
                <a href="https://amzn.to/4dwj6uc" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/91MAequ2koL._SY466_.jpg" alt="Volume 2">
                <h3>Volume 2</h3>
                <a href="https://amzn.to/4e3FURZ" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/816m3mfx21L._SY466_.jpg" alt="Volume 3">
                <h3>Volume 3</h3>
                <a href="https://amzn.to/3O7SmFZ" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71VS-OuXOjL._SY466_.jpg" alt="Volume 4">
                <h3>Volume 4</h3>
                <a href="https://amzn.to/3Q284Tx" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71c-+BcZ-eL._SY466_.jpg" alt="Volume 5">
                <h3>Volume 5</h3>
                <a href="https://amzn.to/41fVClG" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71IzFZtdXqL._AC_SX522_.jpg" alt="Volume 6">
                <h3>Volume 6</h3>
                <a href="https://amzn.to/4twaYhT" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/718uO+aYN6L._SY342_.jpg" alt="Volume 7">
                <h3>Volume 7</h3>
                <a href="https://amzn.to/4shD935" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71derwm7eFL._SY342_.jpg" alt="Volume 8">
                <h3>Volume 8</h3>
                <a href="https://amzn.to/41fykwk" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71qJzYr9icL._SY466_.jpg" alt="Volume 9">
                <h3>Volume 9</h3>
                <a href="https://amzn.to/4v8D7gN" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61L2aeTkrWL._SY425_.jpg" alt="Volume 10">
                <h3>Volume 10</h3>
                <a href="https://amzn.to/48t9uwC" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71zBO2JVYUL._SY466_.jpg" alt="Volume 11">
                <h3>Volume 11</h3>
                <a href="https://amzn.to/4e5ZahL" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71R3CjwSNlL._SY466_.jpg" alt="Volume 12">
                <h3>Volume 12</h3>
                <a href="https://amzn.to/41kqMIy" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71GKUtAYZ-L._SY466_.jpg" alt="Volume 13">
                <h3>Volume 13</h3>
                <a href="https://amzn.to/3PQsPBI" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71OiUJVg1FL._SY466_.jpg" alt="Volume 14">
                <h3>Volume 14</h3>
                <a href="https://amzn.to/41fymEs" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71gQHRPD8gL._SY466_.jpg" alt="Volume 15">
                <h3>Volume 15</h3>
                <a href="https://amzn.to/3PNhdzr" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71ASM5vNQKL._SY466_.jpg" alt="Volume 16">
                <h3>Volume 16</h3>
                <a href="https://amzn.to/483WrSv" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61A9NjXSARL._SY466_.jpg" alt="Volume 17">
                <h3>Volume 17</h3>
                <a href="https://amzn.to/4mw9r9v" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/7191y21JFZL._SY466_.jpg" alt="Volume 18">
                <h3>Volume 18</h3>
                <a href="https://amzn.to/4ses9na" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71o-XdAz7lL._SY466_.jpg" alt="Volume 19">
                <h3>Volume 19</h3>
                <a href="https://amzn.to/3OpKfEN" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61fOmH2dU-L._SY342_.jpg" alt="Volume 20">
                <h3>Volume 20</h3>
                <a href="https://amzn.to/4sUIleg" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

        </div>
    </div>
    <div class="footer">
        <p>© Mundo Mangá Promos - Links de Associado Amazon</p>
    </div>
</body>
</html>

```
</file>

### Arquivo: `series/111233/index.html`
<file path="series/111233/index.html" lines="191">
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Série - Mundo Mangá Promos</title>
    <style>
        :root {
            --primary: #F28C4A;
            --bg: #f4f4f9;
            --text: #333;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg);
            color: var(--text);
            margin: 0;
            padding: 0;
        }
        header {
            background-color: var(--primary);
            color: white;
            padding: 20px;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        .container {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 20px;
        }
        .card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: transform 0.2s;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 15px;
            text-align: center;
        }
        .card:hover {
            transform: translateY(-5px);
        }
        .card img {
            max-width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 8px;
            margin-bottom: 15px;
        }
        .card h3 {
            margin: 0 0 15px 0;
            font-size: 1.1rem;
            flex-grow: 1;
        }
        .btn {
            background-color: #28a745;
            color: white;
            text-decoration: none;
            padding: 10px 20px;
            border-radius: 8px;
            font-weight: bold;
            width: 100%;
            box-sizing: border-box;
            display: inline-block;
        }
        .btn:hover {
            background-color: #218838;
        }
        .footer {
            text-align: center;
            padding: 20px;
            color: #666;
            margin-top: 40px;
        }
    </style>
</head>
<body>
    <header>
        <h1>📚 Coleção Completa</h1>
        <p>Complete a sua estante com os melhores preços!</p>
    </header>
    
    <div class="container">
        <div class="grid">

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61Vpc6U1onL._SY342_.jpg" alt="Volume 01">
                <h3>Volume 01</h3>
                <a href="https://amzn.to/4bOHOVl" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61od9N2ZonL._SY342_.jpg" alt="Volume 02">
                <h3>Volume 02</h3>
                <a href="https://amzn.to/4bZAh4H" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/619ngn8-zTL._SY342_.jpg" alt="Volume 3">
                <h3>Volume 3</h3>
                <a href="https://amzn.to/4c4STAi" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61Dq71wS+xL._SY342_.jpg" alt="Volume 4">
                <h3>Volume 4</h3>
                <a href="https://amzn.to/4clCTLI" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61PzmPNYBkL._SY342_.jpg" alt="Volume 6">
                <h3>Volume 6</h3>
                <a href="https://amzn.to/4bYCMEs" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61OuS+jf5+L._SY342_.jpg" alt="Volume 7">
                <h3>Volume 7</h3>
                <a href="https://amzn.to/4tu7XPe" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/619b9cFfxlL._SY342_.jpg" alt="Volume 8">
                <h3>Volume 8</h3>
                <a href="https://amzn.to/41dYaAJ" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61FtoLKgaVL._SY466_.jpg" alt="Volume 9">
                <h3>Volume 9</h3>
                <a href="https://amzn.to/4clEmlc" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61WBwYyYFbL._SY466_.jpg" alt="Volume 11">
                <h3>Volume 11</h3>
                <a href="https://amzn.to/4c4SWfs" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61EFZs4GCxL._SY466_.jpg" alt="Volume 13">
                <h3>Volume 13</h3>
                <a href="https://amzn.to/3OectCp" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61H955GvGuL._SY466_.jpg" alt="Volume 14">
                <h3>Volume 14</h3>
                <a href="https://amzn.to/4dqkZIP" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61khlfaSH3L._SY466_.jpg" alt="Volume 15">
                <h3>Volume 15</h3>
                <a href="https://amzn.to/4clFB3Q" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/51EEsqndE-L._SY466_.jpg" alt="Volume 17">
                <h3>Volume 17</h3>
                <a href="https://amzn.to/4c33BaK" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61p4HJVYD5L._SY466_.jpg" alt="Volume 18">
                <h3>Volume 18</h3>
                <a href="https://amzn.to/4clFWUa" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61zbF0A82+L._SY466_.jpg" alt="Volume 19">
                <h3>Volume 19</h3>
                <a href="https://amzn.to/4smZAEg" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

        </div>
    </div>
    <div class="footer">
        <p>© Mundo Mangá Promos - Links de Associado Amazon</p>
    </div>
</body>
</html>

```
</file>

### Arquivo: `series/30012/index.html`
<file path="series/30012/index.html" lines="215">
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Série - Mundo Mangá Promos</title>
    <style>
        :root {
            --primary: #F28C4A;
            --bg: #f4f4f9;
            --text: #333;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg);
            color: var(--text);
            margin: 0;
            padding: 0;
        }
        header {
            background-color: var(--primary);
            color: white;
            padding: 20px;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        .container {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 20px;
        }
        .card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: transform 0.2s;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 15px;
            text-align: center;
        }
        .card:hover {
            transform: translateY(-5px);
        }
        .card img {
            max-width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 8px;
            margin-bottom: 15px;
        }
        .card h3 {
            margin: 0 0 15px 0;
            font-size: 1.1rem;
            flex-grow: 1;
        }
        .btn {
            background-color: #28a745;
            color: white;
            text-decoration: none;
            padding: 10px 20px;
            border-radius: 8px;
            font-weight: bold;
            width: 100%;
            box-sizing: border-box;
            display: inline-block;
        }
        .btn:hover {
            background-color: #218838;
        }
        .footer {
            text-align: center;
            padding: 20px;
            color: #666;
            margin-top: 40px;
        }
    </style>
</head>
<body>
    <header>
        <h1>📚 Coleção Completa</h1>
        <p>Complete a sua estante com os melhores preços!</p>
    </header>
    
    <div class="container">
        <div class="grid">

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/51pAoyagkWL._SY342_.jpg" alt="Volume 01">
                <h3>Volume 01</h3>
                <a href="https://amzn.to/3NJ6tl2" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61AwPiYDeFL._SY425_.jpg" alt="Volume 02">
                <h3>Volume 02</h3>
                <a href="https://amzn.to/3PU9ijI" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/51rAKP1LfUL._SY425_.jpg" alt="Volume 03">
                <h3>Volume 03</h3>
                <a href="https://amzn.to/4m9t9r7" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61Pva8BNYQL._SY342_.jpg" alt="Volume 4">
                <h3>Volume 4</h3>
                <a href="https://amzn.to/4mbUzNh" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61ZGTgwrGUL._SY425_.jpg" alt="Volume 5">
                <h3>Volume 5</h3>
                <a href="https://amzn.to/41OUBRG" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/51BIRDFz8DL._SY342_.jpg" alt="Volume 6">
                <h3>Volume 6</h3>
                <a href="https://amzn.to/3O5Jqkg" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61ZEHA-PUmL._SY342_.jpg" alt="Volume 7">
                <h3>Volume 7</h3>
                <a href="https://amzn.to/3PQsZsO" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/51lsseOn41L._SY522_.jpg" alt="Volume 8">
                <h3>Volume 8</h3>
                <a href="https://amzn.to/3PPzAUl" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/519JUntzWGL._SY425_.jpg" alt="Volume 09">
                <h3>Volume 09</h3>
                <a href="https://amzn.to/4cpURg6" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/615IAFDHF1L._SY342_.jpg" alt="Volume 10">
                <h3>Volume 10</h3>
                <a href="https://amzn.to/4c2OcXO" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/51q0N60GU0L._SY342_.jpg" alt="Volume 11">
                <h3>Volume 11</h3>
                <a href="https://amzn.to/3PS0qLB" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61RLCqazhHL._SY342_.jpg" alt="Volume 12">
                <h3>Volume 12</h3>
                <a href="https://amzn.to/4c3OQUT" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/51dY4wzESEL._SY342_.jpg" alt="Volume 13">
                <h3>Volume 13</h3>
                <a href="https://amzn.to/4dvAoHQ" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/51KBfZw9RCL._SY342_.jpg" alt="Volume 14">
                <h3>Volume 14</h3>
                <a href="https://amzn.to/4twj9uF" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/616YIZXCnaL._SY342_.jpg" alt="Volume 15">
                <h3>Volume 15</h3>
                <a href="https://amzn.to/47I2U5e" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61XBVSb53wL._SY342_.jpg" alt="Volume 16">
                <h3>Volume 16</h3>
                <a href="https://amzn.to/4c7qR7r" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61U89Xmh-SL._SY342_.jpg" alt="Volume 17">
                <h3>Volume 17</h3>
                <a href="https://amzn.to/4tzxQ0a" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61qTDw9-o5L._SY466_.jpg" alt="Volume 18">
                <h3>Volume 18</h3>
                <a href="https://amzn.to/3NOYov7" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/51m0HMBNahL._SY466_.jpg" alt="Volume 19">
                <h3>Volume 19</h3>
                <a href="https://amzn.to/47Fa9Lh" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

        </div>
    </div>
    <div class="footer">
        <p>© Mundo Mangá Promos - Links de Associado Amazon</p>
    </div>
</body>
</html>

```
</file>

### Arquivo: `series/30025/index.html`
<file path="series/30025/index.html" lines="221">
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Série - Mundo Mangá Promos</title>
    <style>
        :root {
            --primary: #57310a;
            --bg: #f4f4f9;
            --text: #333;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg);
            color: var(--text);
            margin: 0;
            padding: 0;
        }
        header {
            background-color: var(--primary);
            color: white;
            padding: 20px;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        .container {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 20px;
        }
        .card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: transform 0.2s;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 15px;
            text-align: center;
        }
        .card:hover {
            transform: translateY(-5px);
        }
        .card img {
            max-width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 8px;
            margin-bottom: 15px;
        }
        .card h3 {
            margin: 0 0 15px 0;
            font-size: 1.1rem;
            flex-grow: 1;
        }
        .btn {
            background-color: #28a745;
            color: white;
            text-decoration: none;
            padding: 10px 20px;
            border-radius: 8px;
            font-weight: bold;
            width: 100%;
            box-sizing: border-box;
            display: inline-block;
        }
        .btn:hover {
            background-color: #218838;
        }
        .footer {
            text-align: center;
            padding: 20px;
            color: #666;
            margin-top: 40px;
        }
    </style>
</head>
<body>
    <header>
        <h1>📚 Coleção Completa</h1>
        <p>Complete a sua estante com os melhores preços!</p>
    </header>
    
    <div class="container">
        <div class="grid">

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61yvu+BbxvL._SY425_.jpg" alt="Volume 1">
                <h3>Volume 1</h3>
                <a href="https://amzn.to/4m3HyFe" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/617-gUUpJ4L._SY425_.jpg" alt="Volume 2">
                <h3>Volume 2</h3>
                <a href="https://amzn.to/3Q2KyWx" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61ab9fFA9ZL._SY425_.jpg" alt="Volume 3">
                <h3>Volume 3</h3>
                <a href="https://amzn.to/3PXJsLF" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/618A16aA12L._SY425_.jpg" alt="Volume 4">
                <h3>Volume 4</h3>
                <a href="https://amzn.to/4bZ6I3f" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61sLlVcjCyL._SY425_.jpg" alt="Volume 5">
                <h3>Volume 5</h3>
                <a href="https://amzn.to/4dqkONF" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/616Ht4scaTL._SY425_.jpg" alt="Volume 6">
                <h3>Volume 6</h3>
                <a href="https://amzn.to/4tqnBLq" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61-OZSHDCTL._SY425_.jpg" alt="Volume 7">
                <h3>Volume 7</h3>
                <a href="https://amzn.to/41LKmgW" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61RPTrzt7QL._SY425_.jpg" alt="Volume 8">
                <h3>Volume 8</h3>
                <a href="https://amzn.to/41bFjq0" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/618DkDAXPCL._SY425_.jpg" alt="Volume 9">
                <h3>Volume 9</h3>
                <a href="https://amzn.to/4sJStGI" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61McUesiHwL._SY425_.jpg" alt="Volume 10">
                <h3>Volume 10</h3>
                <a href="https://amzn.to/3QiCReQ" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61dGfftfjCL._SY425_.jpg" alt="Volume 11">
                <h3>Volume 11</h3>
                <a href="https://amzn.to/3O3qAdI" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61K5N92MQmL._SY425_.jpg" alt="Volume 12">
                <h3>Volume 12</h3>
                <a href="https://amzn.to/4sZCXqn" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61trNXWTCLL._SY425_.jpg" alt="Volume 13">
                <h3>Volume 13</h3>
                <a href="https://amzn.to/4sav2Fi" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61pWGkagQjL._SY425_.jpg" alt="Volume 14">
                <h3>Volume 14</h3>
                <a href="https://amzn.to/4thKvEw" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61f-POLoDhL._SY425_.jpg" alt="Volume 15">
                <h3>Volume 15</h3>
                <a href="https://amzn.to/417UWyG" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/618+peSaBcL._SY425_.jpg" alt="Volume 16">
                <h3>Volume 16</h3>
                <a href="https://amzn.to/4tl3SfZ" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/619yHSZ6AYL._SY425_.jpg" alt="Volume 17">
                <h3>Volume 17</h3>
                <a href="https://amzn.to/4c4SOfY" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61OyC517mLL._SY425_.jpg" alt="Volume 18">
                <h3>Volume 18</h3>
                <a href="https://amzn.to/41LKq0a" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61vWUK+zO3L._SY425_.jpg" alt="Volume 19">
                <h3>Volume 19</h3>
                <a href="https://amzn.to/47ASTXx" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/614OaQa+CTL._SY425_.jpg" alt="Volume 20">
                <h3>Volume 20</h3>
                <a href="https://amzn.to/41cjsP5" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

        </div>
    </div>
    <div class="footer">
        <p>© Mundo Mangá Promos - Links de Associado Amazon</p>
    </div>
</body>
</html>

```
</file>

### Arquivo: `series/30908/index.html`
<file path="series/30908/index.html" lines="119">
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Série - Mundo Mangá Promos</title>
    <style>
        :root {
            --primary: #F28C4A;
            --bg: #f4f4f9;
            --text: #333;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg);
            color: var(--text);
            margin: 0;
            padding: 0;
        }
        header {
            background-color: var(--primary);
            color: white;
            padding: 20px;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        .container {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 20px;
        }
        .card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: transform 0.2s;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 15px;
            text-align: center;
        }
        .card:hover {
            transform: translateY(-5px);
        }
        .card img {
            max-width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 8px;
            margin-bottom: 15px;
        }
        .card h3 {
            margin: 0 0 15px 0;
            font-size: 1.1rem;
            flex-grow: 1;
        }
        .btn {
            background-color: #28a745;
            color: white;
            text-decoration: none;
            padding: 10px 20px;
            border-radius: 8px;
            font-weight: bold;
            width: 100%;
            box-sizing: border-box;
            display: inline-block;
        }
        .btn:hover {
            background-color: #218838;
        }
        .footer {
            text-align: center;
            padding: 20px;
            color: #666;
            margin-top: 40px;
        }
    </style>
</head>
<body>
    <header>
        <h1>📚 Coleção Completa</h1>
        <p>Complete a sua estante com os melhores preços!</p>
    </header>
    
    <div class="container">
        <div class="grid">

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/613BkZ9s3jL._AC_UL320_.jpg" alt="Volume 1">
                <h3>Volume 1</h3>
                <a href="https://amzn.to/3MRqGV2" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61VbIV64VSL._AC_UL320_.jpg" alt="Volume 2">
                <h3>Volume 2</h3>
                <a href="https://amzn.to/4u1DbxY" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71U2UKZrGmL._AC_UL320_.jpg" alt="Volume 3">
                <h3>Volume 3</h3>
                <a href="https://amzn.to/40zDVNr" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

        </div>
    </div>
    <div class="footer">
        <p>© Mundo Mangá Promos - Links de Associado Amazon</p>
    </div>
</body>
</html>

```
</file>

### Arquivo: `series/74489/index.html`
<file path="series/74489/index.html" lines="149">
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Série - Mundo Mangá Promos</title>
    <style>
        :root {
            --primary: #F28C4A;
            --bg: #f4f4f9;
            --text: #333;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg);
            color: var(--text);
            margin: 0;
            padding: 0;
        }
        header {
            background-color: var(--primary);
            color: white;
            padding: 20px;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        .container {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 20px;
        }
        .card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: transform 0.2s;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 15px;
            text-align: center;
        }
        .card:hover {
            transform: translateY(-5px);
        }
        .card img {
            max-width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 8px;
            margin-bottom: 15px;
        }
        .card h3 {
            margin: 0 0 15px 0;
            font-size: 1.1rem;
            flex-grow: 1;
        }
        .btn {
            background-color: #28a745;
            color: white;
            text-decoration: none;
            padding: 10px 20px;
            border-radius: 8px;
            font-weight: bold;
            width: 100%;
            box-sizing: border-box;
            display: inline-block;
        }
        .btn:hover {
            background-color: #218838;
        }
        .footer {
            text-align: center;
            padding: 20px;
            color: #666;
            margin-top: 40px;
        }
    </style>
</head>
<body>
    <header>
        <h1>📚 Coleção Completa</h1>
        <p>Complete a sua estante com os melhores preços!</p>
    </header>
    
    <div class="container">
        <div class="grid">

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/91s66otV7wL._SY425_.jpg" alt="Volume 01">
                <h3>Volume 01</h3>
                <a href="https://amzn.to/4ccLQWv" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/91cTmPrhL7L._SY425_.jpg" alt="Volume 02">
                <h3>Volume 02</h3>
                <a href="https://amzn.to/41fzasY" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/912NMm8SGeL._SY425_.jpg" alt="Volume 03">
                <h3>Volume 03</h3>
                <a href="https://amzn.to/4caq5Xk" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/91AusNfUg-L._SY425_.jpg" alt="Volume 04">
                <h3>Volume 04</h3>
                <a href="https://amzn.to/3Q75jAp" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/91LHDwh8ntL._SY425_.jpg" alt="Volume 05">
                <h3>Volume 05</h3>
                <a href="https://amzn.to/41fZd3c" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/91GSGwMaHkL._SY425_.jpg" alt="Volume 06">
                <h3>Volume 06</h3>
                <a href="https://amzn.to/3O5JSPu" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/81g9wFvxmsL._SY425_.jpg" alt="Volume 07">
                <h3>Volume 07</h3>
                <a href="https://amzn.to/4tuNvxC" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/812L1SGao+L._SY425_.jpg" alt="Volume 08">
                <h3>Volume 08</h3>
                <a href="https://amzn.to/4vbLpnV" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

        </div>
    </div>
    <div class="footer">
        <p>© Mundo Mangá Promos - Links de Associado Amazon</p>
    </div>
</body>
</html>

```
</file>

### Arquivo: `series/86635/index.html`
<file path="series/86635/index.html" lines="269">
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Série - Mundo Mangá Promos</title>
    <style>
        :root {
            --primary: #F28C4A;
            --bg: #f4f4f9;
            --text: #333;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg);
            color: var(--text);
            margin: 0;
            padding: 0;
        }
        header {
            background-color: var(--primary);
            color: white;
            padding: 20px;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        .container {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 20px;
        }
        .card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: transform 0.2s;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 15px;
            text-align: center;
        }
        .card:hover {
            transform: translateY(-5px);
        }
        .card img {
            max-width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 8px;
            margin-bottom: 15px;
        }
        .card h3 {
            margin: 0 0 15px 0;
            font-size: 1.1rem;
            flex-grow: 1;
        }
        .btn {
            background-color: #28a745;
            color: white;
            text-decoration: none;
            padding: 10px 20px;
            border-radius: 8px;
            font-weight: bold;
            width: 100%;
            box-sizing: border-box;
            display: inline-block;
        }
        .btn:hover {
            background-color: #218838;
        }
        .footer {
            text-align: center;
            padding: 20px;
            color: #666;
            margin-top: 40px;
        }
    </style>
</head>
<body>
    <header>
        <h1>📚 Coleção Completa</h1>
        <p>Complete a sua estante com os melhores preços!</p>
    </header>
    
    <div class="container">
        <div class="grid">

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61EP4kOgxyL._SY466_.jpg" alt="Volume 1">
                <h3>Volume 1</h3>
                <a href="https://amzn.to/4lE40F1" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61ZNdHfyYwL._SY466_.jpg" alt="Volume 2">
                <h3>Volume 2</h3>
                <a href="https://amzn.to/4bAOKnG" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61UPAINXR2L._SY466_.jpg" alt="Volume 3">
                <h3>Volume 3</h3>
                <a href="https://amzn.to/47LV62b" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71d3x+sxGML._SY466_.jpg" alt="Volume 4">
                <h3>Volume 4</h3>
                <a href="https://amzn.to/41bshIV" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71TWzybyQ4L._SY466_.jpg" alt="Volume 5">
                <h3>Volume 5</h3>
                <a href="https://amzn.to/4lAhi5b" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61kUsAmv9tL._SY466_.jpg" alt="Volume 6">
                <h3>Volume 6</h3>
                <a href="https://amzn.to/4sSpH6z" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71WsZlEu8pL._SY466_.jpg" alt="Volume 7">
                <h3>Volume 7</h3>
                <a href="https://amzn.to/4sPx52i" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71jkiZ41TrL._SY425_.jpg" alt="Volume 8">
                <h3>Volume 8</h3>
                <a href="https://amzn.to/4dugz3r" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/717jiTyEQVL._SY466_.jpg" alt="Volume 9">
                <h3>Volume 9</h3>
                <a href="https://amzn.to/4uA07EP" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71sKY4RMd0L._SY425_.jpg" alt="Volume 10">
                <h3>Volume 10</h3>
                <a href="https://amzn.to/3NN9513" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61RE+7jfogL._SY425_.jpg" alt="Volume 11">
                <h3>Volume 11</h3>
                <a href="https://amzn.to/4uyv3W8" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71MZwMacplL._SY425_.jpg" alt="Volume 12">
                <h3>Volume 12</h3>
                <a href="https://amzn.to/4uBJ1Xk" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61MjaPhhjuL._SY466_.jpg" alt="Volume 13">
                <h3>Volume 13</h3>
                <a href="https://amzn.to/4lxRyq6" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61UPEJr5yjL._SY425_.jpg" alt="Volume 14">
                <h3>Volume 14</h3>
                <a href="https://amzn.to/4bueeTA" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61qBBPyG+LL._SY342_.jpg" alt="Volume 15">
                <h3>Volume 15</h3>
                <a href="https://amzn.to/4cQ1x7W" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/510jwY7JmRL._SY425_.jpg" alt="Volume 16">
                <h3>Volume 16</h3>
                <a href="https://amzn.to/4sTSMyt" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/51mJqulq2YL._SY425_.jpg" alt="Volume 17">
                <h3>Volume 17</h3>
                <a href="https://amzn.to/4bCh21b" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/511fF9F3Q1L._SY445_SX342_ML2_.jpg" alt="Volume 18">
                <h3>Volume 18</h3>
                <a href="https://amzn.to/3NAbjRc" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://www.manga-news.com/public/images/vols/.Kaguya-sama_Love_is_War_T19_-_Pika_large.jpg" alt="Volume 19">
                <h3>Volume 19</h3>
                <a href="https://amzn.to/4bvZ6F4" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61fc7QC6w4L._SY342_.jpg" alt="Volume 20">
                <h3>Volume 20</h3>
                <a href="https://amzn.to/4biVc3P" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/6145ZOO9ryL._SY342_.jpg" alt="Volume 21">
                <h3>Volume 21</h3>
                <a href="https://amzn.to/4lEg6xM" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://www.manga-news.com/public/images/vols/.Kaguya-sama_Love_is_War_T22-_Pika_large.webp" alt="Volume 22">
                <h3>Volume 22</h3>
                <a href="https://amzn.to/4rJrFoT" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61sYvsiMfyL._SY342_.jpg" alt="Volume 23">
                <h3>Volume 23</h3>
                <a href="https://amzn.to/4rJrFoT" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/617NHwQCiZL._SY342_.jpg" alt="Volume 24">
                <h3>Volume 24</h3>
                <a href="https://amzn.to/3NI0tZC" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/6108Z-qqSuL._SY342_.jpg" alt="Volume 25">
                <h3>Volume 25</h3>
                <a href="https://amzn.to/4dopNyc" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://www.manga-news.com/public/images/vols/.Kaguya-sama_Love_is_War_T26_-_Pika_large.webp" alt="Volume 26">
                <h3>Volume 26</h3>
                <a href="https://amzn.to/4bxyT9l" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://www.manga-news.com/public/images/vols/.Kaguya-sama_Love_is_War_T27_-_Pika_large.webp" alt="Volume 27">
                <h3>Volume 27</h3>
                <a href="https://amzn.to/4rXnDcJ" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61YFnniALQL._SY342_.jpg" alt="Volume 28">
                <h3>Volume 28</h3>
                <a href="https://amzn.to/419KWVt" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

        </div>
    </div>
    <div class="footer">
        <p>© Mundo Mangá Promos - Links de Associado Amazon</p>
    </div>
</body>
</html>

```
</file>

### Arquivo: `series/98235/index.html`
<file path="series/98235/index.html" lines="221">
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Série - Mundo Mangá Promos</title>
    <style>
        :root {
            --primary: #F28C4A;
            --bg: #f4f4f9;
            --text: #333;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg);
            color: var(--text);
            margin: 0;
            padding: 0;
        }
        header {
            background-color: var(--primary);
            color: white;
            padding: 20px;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        .container {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 20px;
        }
        .card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: transform 0.2s;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 15px;
            text-align: center;
        }
        .card:hover {
            transform: translateY(-5px);
        }
        .card img {
            max-width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 8px;
            margin-bottom: 15px;
        }
        .card h3 {
            margin: 0 0 15px 0;
            font-size: 1.1rem;
            flex-grow: 1;
        }
        .btn {
            background-color: #28a745;
            color: white;
            text-decoration: none;
            padding: 10px 20px;
            border-radius: 8px;
            font-weight: bold;
            width: 100%;
            box-sizing: border-box;
            display: inline-block;
        }
        .btn:hover {
            background-color: #218838;
        }
        .footer {
            text-align: center;
            padding: 20px;
            color: #666;
            margin-top: 40px;
        }
    </style>
</head>
<body>
    <header>
        <h1>📚 Coleção Completa</h1>
        <p>Complete a sua estante com os melhores preços!</p>
    </header>
    
    <div class="container">
        <div class="grid">

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/81BHQ2Nr1KL._SY466_.jpg" alt="Volume 1">
                <h3>Volume 1</h3>
                <a href="https://amzn.to/3NyBrw8" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71LWUU0JzuL._SY342_.jpg" alt="Volume 2">
                <h3>Volume 2</h3>
                <a href="https://amzn.to/4v3pDTm" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61dqo1XDeWL._SY425_.jpg" alt="Volume 3">
                <h3>Volume 3</h3>
                <a href="https://amzn.to/4dqFMvT" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61+FQyPJ4YL._SY425_.jpg" alt="Volume 4">
                <h3>Volume 4</h3>
                <a href="https://amzn.to/4tehTMp" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61SXNty1WKS._SY342_.jpg" alt="Volume 5">
                <h3>Volume 5</h3>
                <a href="https://amzn.to/4dlQNOT" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61o+7ENVxqL._SY425_.jpg" alt="Volume 6">
                <h3>Volume 6</h3>
                <a href="https://amzn.to/3PDzW0g" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61L+xOON+mL._SY342_.jpg" alt="Volume 7">
                <h3>Volume 7</h3>
                <a href="https://amzn.to/3QbJLCD" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/71U4JDqH2JL._SY342_.jpg" alt="Volume 8">
                <h3>Volume 8</h3>
                <a href="https://amzn.to/4dTXzeW" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61wxhQEhy0L._SY425_.jpg" alt="Volume 9">
                <h3>Volume 9</h3>
                <a href="https://amzn.to/3NBNfOd" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61Y3bTLCaqL._SY425_.jpg" alt="Volume 10">
                <h3>Volume 10</h3>
                <a href="https://amzn.to/4s1JrUx" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61iXSO7kQ0L._SY425_.jpg" alt="Volume 11">
                <h3>Volume 11</h3>
                <a href="https://amzn.to/4spkUch" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61DyOZERM5L._SY466_.jpg" alt="Volume 12">
                <h3>Volume 12</h3>
                <a href="https://amzn.to/4s8cJkl" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61YvTgGSziL._SY342_.jpg" alt="Volume 13">
                <h3>Volume 13</h3>
                <a href="https://amzn.to/418V9l9" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61FbAS+UUeL._SY425_.jpg" alt="Volume 14">
                <h3>Volume 14</h3>
                <a href="https://amzn.to/4v3qrYo" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61AMBjGWVEL._SY425_.jpg" alt="Volume 15">
                <h3>Volume 15</h3>
                <a href="https://amzn.to/4tkchjZ" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61GkdpL3GLL._SY425_.jpg" alt="Volume 16">
                <h3>Volume 16</h3>
                <a href="https://amzn.to/4v3Iaic" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/611AGf9j08L._SY425_.jpg" alt="Volume 17">
                <h3>Volume 17</h3>
                <a href="https://amzn.to/3PGpO6R" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/51-SOW4jFrL._SY425_.jpg" alt="Volume 18">
                <h3>Volume 18</h3>
                <a href="https://amzn.to/4sQM6Sg" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61VcnusUOQL._SY425_.jpg" alt="Volume 19">
                <h3>Volume 19</h3>
                <a href="https://amzn.to/47CwKbo" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

            <div class="card">
                <img src="https://m.media-amazon.com/images/I/61Mv6Z4oKmL._SY425_.jpg" alt="Volume 20">
                <h3>Volume 20</h3>
                <a href="https://amzn.to/3PHxMwD" target="_blank" class="btn">🛒 Comprar na Amazon</a>
            </div>

        </div>
    </div>
    <div class="footer">
        <p>© Mundo Mangá Promos - Links de Associado Amazon</p>
    </div>
</body>
</html>

```
</file>
