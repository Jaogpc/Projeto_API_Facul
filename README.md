# Projeto_API_Facul
Projeto de utilização de API em um aplicativo mobile.

# Descrição: 
O projeto consiste na utilização de uma API a escolha e sua exibição na tela do aplicativo.

# API:
A API escolhida foi a APOD(Atronomic Picture of the Day) da Nasa que exibe uma foto tirada no dia em que é feita a requisição.

<h2>Chave da API: </h2>
A chave é enviada particularmente por email quando requirida. Além disso, sua manipulação é bem simples e prática.

<h2>Implementação da chave: </h2>
Seu requerimento é feito através do seguinte jeito:

``` ruby
public class MainActivity extends AppCompatActivity {

    private static final String BASE_URL = "https://api.nasa.gov/";
    private static final String API_KEY = "DEMO_KEY"; (chave particular)
```

A key é chamada da seguinte forma na classe ApodApi.java:

``` ruby
public interface ApodApi {
    @GET("planetary/apod")
    Call<Apod> getApod(@Query("api_key") String apiKey);
}
```

# Resultado: 

<h2>Tela: </h2>

![6d22de68-89e2-4328-b6cb-ee64d5744ad9](https://github.com/user-attachments/assets/c4f9994d-725a-4c99-a107-82f2fc686d45)

<h2>Descrição da tela: </h2>

 - No topo da tela é exibida a imagem capturada.
 - Abaixo o título da imagem.
 - Por último, um texto sobre a imagem.
