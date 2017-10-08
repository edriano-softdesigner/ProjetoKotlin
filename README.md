# ProjetoKotlin
Códigos Kotlin
data class Pessoa(val nome: String, // Classe data.
                 val idade: Int? = null) // Tipo nullable(Int?); o valor default para argumento.
fun main(args: Array<String>){ // Função de nível superior.
    val pessoas = listOf(Pessoa("Alice"),
                        Pessoa("Bob", idade = 29)) // Argumento nomeado.
    val pessoamaisvelha = pessoas.maxBy {it.idade?:0} // Expressão lambda; operador Elvis.
    println("A pessoa mais velha é : $pessoamaisvelha") // Template de string.
}
// The oldest is: Person(name=Bob, age=29) // toString gerado automaticamente.
