class Atleta {
  constructor(nome, idade, peso, altura, notas) {
    this.nome = nome;
    this.idade = idade;
    this.peso = peso;
    this.altura = altura;
    this.notas = notas;
  }

  // Método para calcular a categoria do atleta
  calculaCategoria() {
    if (this.idade >= 9 && this.idade <= 11) {
      return "Infantil";
    } else if (this.idade >= 12 && this.idade <= 13) {
      return "Juvenil";
    } else if (this.idade >= 14 && this.idade <= 15) {
      return "Intermediário";
    } else if (this.idade >= 16 && this.idade <= 30) {
      return "Adulto";
    } else {
      return "Sem categoria";
    }
  }

  // Método para calcular o IMC do atleta
  calculaIMC() {
    return this.peso / (this.altura * this.altura);
  }

  // Método para calcular a média válida do atleta
  calculaMediaValida() {
    let media = 0
    this.notas = this.notas.sort()
    this.notas.shift()
    this.notas.pop()
      this.notas.map(function(nota){
      return media = media + nota
    })

    return media / this.notas.length
  }

  // Métodos para obter os atributos do atleta
  obtemNomeAtleta() {
    return this.nome;
  }

  obtemIdadeAtleta() {
    return this.idade;
  }''

  obtemPesoAtleta() {
    return this.peso;
  }

  obtemAlturaAtleta() {
    return this.altura;
  }

  obtemNotasAtleta() {
    return this.notas;
  }

  obtemCategoria() {
    return this.calculaCategoria();
  }

  obtemIMC() {
    return this.calculaIMC();
  }

  obtemMediaValida() {
    return this.calculaMediaValida();
  }
}
const atleta = new Atleta("Cesar Abascal", 30, 80, 1.70, [10, 9.34, 8.42, 10, 7.88]);
console.log("Nome: " + atleta.obtemNomeAtleta())
console.log("Idade: " + atleta.obtemIdadeAtleta())
console.log("Peso: " + atleta.obtemPesoAtleta())
console.log("Altura: " + atleta.obtemAlturaAtleta())
console.log("Notas: " + "[" + atleta.obtemNotasAtleta()+"]")
console.log("Categoria: " + atleta.obtemCategoria())
console.log("IMC: " + atleta.obtemIMC())
console.log("Média válida: " + atleta.obtemMediaValida())
