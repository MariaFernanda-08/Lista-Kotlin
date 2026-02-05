# Lista Kotlin 🖥️

## Exercício 1 - Cálculo e Classificação do IMC 🏋️‍♀️
```Kotlin
fun main() {

    print("Digite seu peso(kg):")
    val peso = readln().toFloat()
    
    print("Digite sua altura(m):")
    val altura = readln().toFloat()
    
    val imc = peso/(altura * altura)
    
    if (imc <= 18.5){
        print("Abaixo do peso - IMC: $imc kg/m²")
    } else if (imc > 18.5 && imc <= 24.9){
        print("Peso normal - IMC: $imc kg/m²")
    } else if(imc >= 25 && imc <= 29.9 ){
        print("Sobrepeso - IMC: $imc kg/m²")
    } else{
        print("Obesidade - IMC: $imc kg/m²")
    }  
   
```
---
## Exercício 2 - Construtora Prudente S.A 🏗️
#### A) Cálculo do Terreno 🏠
```Kotlin  
fun main() {    
    //Cálculo da Área
    print("Digite o comprimento do terreno(m):")
    val lado1 = readln().toInt()
    print("Digite a largura do terreno(m):")
    val lado2 = readln().toInt()
    
    val area = lado1 * lado2
    
    println("A área do terreno é de: $area m².")
```
#### B) Profissionais 👨‍🏭
```Kotlin
    //Cálculo dos Profissionais
    val mestreObra = 1
    val engenheiros = (area * 1)/100
    val serventes = (area * 2)/10
    
    if (area >= 10 && area <= 99){
        println("Sua obra terá $serventes serventes e $mestreObra mestre de obra.")
    } else if(area >= 100) {
        println("Sua obra terá $engenheiros engenheiros, $serventes serventes e $mestreObra mestre de obra.")
    } else{
        println("A construtora não fará acordos, apenas a partir de 10m².")  
    }    
```
#### C) Preço 💵
```Kotlin
   //Cálculo do Preço da Obra
    print("Quantos quartos sem suíte você quer?:")
    val quartosSemSuites = readln().toInt()
    
    print("Quantos quartos com suíte você quer?:")
    val quartosComSuites = readln().toInt()
    
    print("Quantos banheiros você quer?:")
    val banheiros = readln().toInt()
    
    print("Quantas áreas de serviço você quer?:")
    val areasServico = readln().toInt()
    
    print("Quantas piscinas você quer?:")
    val piscina = readln().toInt()
    
    val valorArea = (area/10) * 4500 //valor a cada 10m²
    
```
#### D) Mão de Obra 🧱
```Kotlin
   val maoDeObra = (mestreObra * 3500) + (serventes * 1900) + (engenheiros * 11000) 
```
#### E) Relatório 🧾
```Kotlin
   //Serviços
    val valorQuartosSemSuite = quartosSemSuites * 12000
    val valorQuartosComSuite = quartosComSuites * 17000
    val valorBanheiros = banheiros * 5000
    val valorAreasServico = areasServico * 15000
    val valorPiscina = piscina * 27550

    //Preços
    val servicos = valorQuartosSemSuite + valorQuartosComSuite + valorBanheiros + valorAreasServico + valorPiscina
    val valorTotal = valorArea + valorQuartosSemSuite + valorQuartosComSuite + valorBanheiros + valorAreasServico + valorPiscina
    val valorObra = valorTotal + maoDeObra
    
    val lucro = (valorObra - maoDeObra) * 25/100
    
    print("Relatório: \n - Valor gasto em serviços: R$ $servicos,00 \n - Valor da mão de obra: R$ $maoDeObra,00")
    print("\n - Valor total(sem a mão de obra): R$ $valorTotal,00 \n - Valor total(com mão de obra): R$ $valorObra,00")
    print("\n - Lucro da Empresa Prudente S.A: R$ $lucro,00")
}
```
