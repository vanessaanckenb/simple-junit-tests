# Simple JUnit5 tests

<br/>

Simple, but very usefull, Junit5 tests from Alura course.

<br/>
<br/>

# Testes Simples do JUnit5

<br/>

Este é apenas um exemplo simples de testes unitários usando o Junit5.

Código do curso do Alura, apenas um exemplo simples, mas bem útil, até eu ter tempo de esquematizar um projeto mais bem elaborado com testes mais elaborados.

<br/>
<br/>

JUnit é a biblioteca padrão do Java

As ides tem integração nativa com o Junit, se você coloca @Test as ides já reconhecem e adicionam o biblioteca no projeto (tem os jars do junit embutido no eclipse e ja vincula ao projeto), mas não é a melhor maneira de adicionar a biblioteca.

a melhor forma é adicionando a dependência atraves do maven.

<br/>
<br/>


Padrão: nome da classe a ser testada com Test no final

<br/>
<br/>

Importante ressaltar que o package do JUnit 5 mudou

org.junit.jupiter.api.

e não é recomentado mais usar os Assert das versões passadas (foram mantidos apenas para não quebrar as versões anteriores, mas não devem ser usados), agora é Assertions (org.junit.jupiter.api.Assertions)


<br/>
<br/>


TDD

Test Driven Development

Desenvolvimento guiado pelo teste

<br/>


teste -> implementacao -> refatoração -> teste -> ...

<br/>
<br/>


@BeforeEach

método para ser chamado antes de cada um dos métodos de teste.

<br/>

@AfterEach

método para ser chamado depois de cada um dos métodos de teste.

<br/>

@BeforeAll

método para ser chamado uma vez antes de executar os outros métodos.

<br/>

@AfterAll

método para ser chamado uma vez depois de executar os outros métodos.

<br/>
<br/>

Exemplo:
```
public class ReajusteServiceTest {

	private ReajusteService service;
	private Funcionario fulano;

	@BeforeEach
	public void inicializar() {
		this.service = new ReajusteService();
		this.fulano = new Funcionario("Fulano", LocalDate.now(), new BigDecimal("2000.00"));
	}
	
	...
}
```


<br/>

-----------------------------------------

<br/>

Apesar de simples, o código e os testes, são bem úteis e explicativos.

É interessante ver também no projeto como os ifs foram evitados, sendo colocados no Enum Desempenho, cada um com sua responsabilidade.



