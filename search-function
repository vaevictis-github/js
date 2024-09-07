function buscar() {

    // Obtém o elemento da seção onde os resultados serão exibidos
    let section = document.getElementById("resultados-pesquisa")
    
    // Obtém o valor digitado no campo de pesquisa
    let fieldSearch = document.getElementById("campo-pesquisa").value

    // Inicializa variáveis para armazenar resultados e informações
    let results = ""
    let title = ""
    let description = ""

    // Loop através de cada item no array de dados (presumivelmente chamado 'data')
    for (let item of data) {

        // Converte o título e a descrição do item para minúsculas
        title = item.title.toLowerCase()
        description = item.description.toLowerCase()

        // Se o campo de pesquisa estiver vazio, exibe uma mensagem e encerra a função
        if (!fieldSearch) {
            section.innerHTML = "Digite algum valor no campo de pesquisa."
            return
        }

        // Converte o termo de pesquisa para minúsculas
        fieldSearch = fieldSearch.toLowerCase()

        // Verifica se o título ou a descrição contém o termo de pesquisa
        if (title.includes(fieldSearch) || description.includes(fieldSearch)) {
            // Se encontrar, adiciona o item aos resultados
            results += `
            <div class="item-resultado">
            <h2>${item.title}</h2>
            <p class="description-meta">${item.description}</p>
            <a href="${item.link}" target="_blank">Saiba mais</a>
            </div>
            `
        }

        // Se nenhum resultado foi encontrado, exibe uma mensagem e encerra a função
        if (!results) {
            section.innerHTML = "Nenhuma banda encontrada."
            return
        }
    }

    // Atualiza a seção com os resultados encontrados
    section.innerHTML = results
}
