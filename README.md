Exemplo do Padrão Adapter: Integração de Dados de Contatos
Este repositório contém uma implementação em Python do Padrão de Projeto Adapter para unificar a leitura de dados armazenados em diferentes formatos de arquivo (XML e JSON). Ele demonstra como adaptar fontes de dados distintas para uma interface comum, facilitando o processamento uniforme.

🛠 Funcionalidades
Padrão de Projeto Adapter: Converte dados em XML e JSON para uma lista unificada de objetos Contact.
Arquitetura Extensível: Suporte a novos formatos de arquivo pode ser adicionado facilmente com novas implementações de FileReader e ContactsAdapter.
Código Limpo e Organizado: Segue princípios de programação orientada a objetos e o princípio SOLID.


📂 Estrutura de Arquivos

.
├── adapter_pattern_002.py   # Script principal que implementa o padrão Adapter
├── contacts.json            # Arquivo de exemplo em JSON
├── contacts.xml             # Arquivo de exemplo em XML
└── README.md                # Documentação do projeto

🔧 Como Executar
Pré-requisitos
Python 3.x instalado no sistema.
Não há dependências externas.
Passos
Clone o repositório:
git clone https://github.com/seu-usuario/adapter-pattern-exemplo.git
cd adapter-pattern-exemplo
Certifique-se de que os arquivos de dados (contacts.json e contacts.xml) estejam no mesmo diretório que o adapter_pattern_002.py.

Execute o script:

python adapter_pattern_002.py
📝 Exemplos de Arquivos de Dados
contacts.json
json

{
    "contacts": [
        {
            "full_name": "John Doe",
            "email": "john.doe@example.com",
            "phone_number": "555-1234",
            "is_friend": true
        },
        {
            "full_name": "Jane Smith",
            "email": "jane.smith@example.com",
            "phone_number": "555-5678",
            "is_friend": false
        },
        {
            "full_name": "Darren Walker",
            "email": "d.walker@example.com",
            "phone_number": "555-9999",
            "is_friend": true
        }
    ]
}
contacts.xml
xml

<contacts>
    <contact>
        <full_name>Patric Doe</full_name>
        <email>patric.doe@example.com</email>
        <phone_number>777-1234</phone_number>
        <is_friend>true</is_friend>
    </contact>
    <contact>
        <full_name>Alex Smith</full_name>
        <email>alex.smith@example.com</email>
        <phone_number>777-5678</phone_number>
        <is_friend>false</is_friend>
    </contact>
</contacts>
📜 Saída Esperada
Ao executar o script, a saída será semelhante a:

plaintext

Patric Doe (patric.doe@example.com) - 777-1234 (Friend)
Alex Smith (alex.smith@example.com) - 777-5678
John Doe (john.doe@example.com) - 555-1234 (Friend)
Jane Smith (jane.smith@example.com) - 555-5678
Darren Walker (d.walker@example.com) - 555-9999 (Friend)
📚 Padrão de Projeto: Adapter
Este projeto demonstra o uso do Padrão de Projeto Adapter, que permite integrar diferentes fontes de dados (XML e JSON) por meio de uma interface comum (ContactsAdapter).

Componentes Principais:
FileReader: Classe base abstrata para leitura de arquivos.
ContactsAdapter: Classe base abstrata para adaptar os dados para uma lista de objetos Contact.
XMLContactsAdapter / JSONContactsAdapter: Adaptadores específicos para os formatos XML e JSON.
Contact: Representa um contato unificado.
🚀 Como Estender o Projeto
Para adicionar suporte a um novo formato de arquivo:

Implemente uma nova subclasse de FileReader para leitura do arquivo.
Implemente uma nova subclasse de ContactsAdapter para transformar os dados.
Integre o novo adaptador ao script principal.

🛡 Licença
Este projeto é licenciado sob a licença MIT.

🤝 Contribuições
Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

💡 Agradecimentos
Este projeto foi inspirado pela necessidade de integrar diferentes formatos de dados de forma estruturada e eficiente, utilizando padrões de design.
