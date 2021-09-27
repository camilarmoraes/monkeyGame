SetErrorMode(2)

SetWindowTitle( "Jogo do macaco" )

SetVirtualResolution( 736, 437)

//tela de fundo
CreateSprite(LoadImage("selva.jpg")) 


//Colocando e tocando música de fundo
LoadMusic(1,"Jungle.wav")
PlayMusic(1,1)

//CreateSprite(LoadImage(""))

imag1 = LoadImage("banana1.png")
imag2 = LoadImage("EggBlue.png")
imag3 = LoadImage("apple1.png")
imag4 = LoadImage("macaco1.png")
imag5 = LoadImage("EggRed.png")

//Criando Sprite e colocando-as em variaveis 
banana = CreateSprite(imag1)
bola = CreateSprite(imag2)
maca = CreateSprite(imag3)
macaco = CreateSprite(imag4)
bola1 = CreateSprite(imag5)

//Definindo tamanho das sprites
SetSpriteSize(banana, 44, 44)
SetSpriteSize(bola, 44, 44)
SetSpriteSize(macaco, 108, 108)
SetSpriteSize(maca,44,44)
SetSpriteSize(bola1,44,44)


//Definindo uma posição inicial fixa
SetSpritePosition(macaco, 300, 330)


//Definindo tipo de colisão caixa
SetSpriteShape(banana, 2)
SetSpriteShape(macaco, 2)
SetSpriteShape(bola, 2)
SetSpriteShape(maca, 2)
SetSpriteShape(bola1, 2)

//Variaveis usaveis
Pontos = 0

do
	//Usando pontuação
    PrintC("Pontos: ")
    PrintC(Pontos)
    
    
    //Definir a posição do macaco por meio do clique do mouse
    if ( GetPointerPressed() = 1) 
		x# = GetPointerX()
		SetSpritePosition(macaco, x#, 330)
	Endif
    
    //Definir as definições da maça
    //------------------------------------------
    SetSpritePosition(maca,Tvariavel,GetSpriteY(maca) + 4.5)
    
    If GetSpriteCollision(macaco,maca) = 1
		Tvariavel = 0
		SetSpritePosition(maca,Tvariavel,0)
		Tvariavel = Random(0,700) //a melhor forma encontrada foi criar uma variavel que recebia um valor random
		Pontos = Pontos + 5
	endif
	
	If GetSpriteY(maca) > 437
		SetSpritePosition(maca,Tvariavel,0)
		Tvariavel = Random(0,700)
	endif		
    
    
    //Definir as definições da banana
    //-----------------------------------------------------
    SetSpritePosition(banana, Xvariavel , GetSpriteY(banana)+ 4.5)
   
	
	//Colisão da banana com o macaco
	If GetSpriteCollision(macaco, banana) = 1
		Xvariavel = 0
		SetSpritePosition(banana, Xvariavel, 0)
		Xvariavel = Random(0,700)
		Pontos = Pontos + 5
	Endif
	
	//Caso não pegue a banana
	If GetSpriteY(banana) > 437
		SetSpritePosition(banana, Xvariavel, 0)
		Xvariavel = Random(0,700)
		
	Endif

	//Definir as definições da bola
	//--------------------------------------------------------
	
	SetSpritePosition(bola, Zvariavel , GetSpriteY(bola)+4.5)
    
    
	//Colisão da bola com macaco
	If GetSpriteCollision(macaco, bola) = 1
		Zvariavel = 0
		SetSpritePosition(bola, Zvariavel, 0)
		Zvariavel = Random(0,700)
		Pontos = Pontos - 5
	Endif
	
	//Caso não pegue a bola
	If GetSpriteY(bola) > 480
		SetSpritePosition(bola, Zvariavel, 0)
		Zvariavel = Random(0,700)
		
	Endif
	
	//Definir as definições da bola1
	//--------------------------------------------------------
	
	SetSpritePosition(bola1, Gvariavel , GetSpriteY(bola1)+4.5)
    
    
	//Colisão da bola com macaco
	If GetSpriteCollision(macaco, bola1) = 1
		Gvariavel = 0
		SetSpritePosition(bola1, Gvariavel, 0)
		Gvariavel = Random(0,700)
		Pontos = Pontos - 5
	Endif
	
	//Caso não pegue a bola
	If GetSpriteY(bola1) > 480
		SetSpritePosition(bola1, Gvariavel, 0)
		Gvariavel = Random(0,700)
		
	Endif
		
		//Caso o tempo passe de 60 segundos ou a potuação fique igual ou menor que -10
		//Coloca todas as sprites em uma posição fixa
		If (Timer () > 60 and pontos < 0)
			SetSpritePosition(banana, 200, 0)
			SetSpritePosition(maca, 50 ,0)
			SetSpritePosition(bola, 400, 0)
			SetSpritePosition(bola1, 600, 0)
			SetSpritePosition(macaco, 300, 330)
			StopMusic()
			
			//Criando uma string para aparecer na tela do jogo
            texto = CreateText("Fim de jogo")
			SetTextSize(texto,50)
			SetTextPosition(texto,200,200)
			SetTextColor(texto,255,0,0,255)
		Endif	
			
		If (Timer () > 60 and pontos > 10)
			SetSpritePosition(banana, 200, 0)
			SetSpritePosition(maca, 50 ,0)
			SetSpritePosition(bola, 400, 0)
			SetSpritePosition(bola1, 600, 0)
			SetSpritePosition(macaco, 300, 330)
			StopMusic()
			
			//Criando uma string para aparecer na tela do jogo
            texto = CreateText("Fim de jogo")
			SetTextSize(texto,50)
			SetTextPosition(texto,200,200)
			SetTextColor(texto,0,255,0,255)
		Endif	
			
    Sync()
loop

