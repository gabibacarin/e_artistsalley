# Loja Lullaboo (e Artist's Alley)
## SCC0219 - 2024.2

Aluna: Gabriela Bacarin Marcondes #10873351
--
### Requisitos

<details>
    <summary>Requisitos do projeto</summary>

- The system must have 2 types of users: Clients and Administrators

- Administrators are responsible for registering/managing administrators, customers, and products/services provided. The application already comes with an account admin with password admin.

- Customers are users who access the system to buy products/services.

- The admin record includes, at least: name, id, phone, email.

- Each customer's record includes, at least: name, id, address, phone, email

- Product/services records include, at least: name, id, photo, description, price, quantity (in stock), and quantity sold.

- Your store may sell products, services or both (you decide)

- Selling Products (or services): Products are selected, their quantity chosen, and are included in a cart. Products are purchased using a credit card number (any number is accepted by the system). The quantity of product sold is subtracted from the quantity in stock and added to the quantity sold. Carts are emptied only on payment or by customers.

- Product/Service Management: Administrators can create/update/read/delete (crud) new products and services. For example, they can change the stock quantity.

- Your functionality: Create a functionality that is specific to your application. It does not have to be something complicated. For instance, if you are selling cars, you may allow users to use an accelerator to hear how each car engine roars up and down.

- The system must provide accessibility requirements and provide good usability. The system must be responsive, meaning that it should complete assigned tasks within a reasonable time.

</details>

Requisitos gerais

- Identidade visual alinhada com os produtos vendidos

- Cadastro de usuário para compra simplificado

- Separação por tipos de produtos (adesivos, prints, marca páginas, bottons) e por subcategorias de cada tipo referente à temática; navegação por tipos e filtros para subcategorias

- Escolher entre entrega do pedido por envio (quando disponível), presencialmente em eventos cadastrados pela administradora ou entrega combinada diretamente com a administradora

- Produtos podem estar em pronta entrega, disponíveis para encomenda ou indisponíveis (esgotados)

- Caso apenas produtos à pronta entrega forem adicionados a um pedido e ele estiver elegível para envio ou retirada em evento, a opção para pagamento deve ser disponibilizada automaticamente

- Caso algum produto no pedido for sob encomenda ou o modo de entrega for à combinar, o pedido deve ser aprovado pela administração antes do pagamento ser disponibilizado para o cliente, garantindo que o combinado pode ser cumprido

- A troca de mensagens se dá diretamente pelo site entre administradora e usuários

Requisitos específicos para administradores

- Possibilidade de fechar a loja, estado em que ela se torna uma vitrine

- Gerador de marca d'água integrado ao carregamento de fotos para evitar plágio/mineração da propriedade intelectual

- Possibilidade de definir individualmente as formas de entrega disponíveis para cada produto, inclusive um número mínimo de produtos iguais para elegibilidade de envio

- Possibilidade de moderação de contas de usuários, inclusive restringir compras, restringir mensagens ou excluir a conta

- Possibilidade de rejeitar pedidos em qualquer momento desde que combinado com o comprador, facilitando possível devolução de dinheiro

- Mecanismos para prevenir spam de compras, cadastros de contas e contas secundárias a serem definidos

### Descrição do Projeto

A loja é direcionada para a venda de produtos de uma artista local, cujo negócio atualmente consiste principalmente em exposições em feiras e eventos que tenham um artist's alley. A ideia do site é estender a possibilidade de compra online e visibilidade para mais pessoas. A maior parte da divulgação é feita por Instagram, portanto, a loja será uma linha auxiliar na presença online. Nota-se que, caso esse formato se prove adequado, pode ser generalizado em um projeto white-label mais tarde para pequenos artistas fazerem suas próprias lojas.


Os produtos consistem em artes físicas, como prints e adesivos, bem como digitais e, eventualmente, comissions de projetos audiovisuais. A entrega é facilitada se a pessoa puder retirar o pedido presencialmente em algum evento em que a artista estará presente (e que estará cadastrado no site como um lugar para entrega). A justificativa é a capacidade de encomendar produtos específicos que não necessariamente estariam disponíveis na venda presencial na ocasião. Além disso, a entrega pode ser feita por envio ou de outra forma a combinar diretamente com a vendedora, a critério da mesma.


Abaixo, o mapa dos caminhos possíveis no site está rascunhado.

![image](https://github.com/user-attachments/assets/ca73b6cf-111f-43b7-9207-35ee0715e209)


Os mockups estão presentes no repositório, no arquivo mocks.psd. Note que eles estão servindo apenas como guias para os componentes que estarão em cada página; o estilo deverá ser mudado para se adequar às demandas da cliente.

O projeto será desenvolvido como uma aplicação React, se valendo dos recursos de componentes para popular o site. Também deve integrar responsividade e recursos para leitura de tela. O contraste provavelmente já será alto por definição do estilo, mas, caso necessário, ferramentas para alto contraste serão adicionadas.

Sobre cada tela:

- Loja - é a tela inicial, a home, na qual um menubar está disponível para a navegação para as outras páginas internas (login, carrinho, perfil - caso logado) e externas, como links para redes sociais da artista. Uma barra de avisos pode ser configurada pela administração para aparecer logo abaixo do menu. Quando a loja estiver fechada, uma mensagem aparecerá e a tela da loja servirá como vitrine. Os produtos estão separados por tipo, podendo ser adesivos, prints, artes digitais, bottons e marca páginas (a princípio). A navegação por esses tipos está em uma barra horizontal que engloba tudo que virá abaixo. A navegação por categorias temáticas está disponível logo antes das imagens dos produtos. As categorias são editáveis pela administração. Por padrão, todos os produtos de um tipo são mostrados em uma página; quando uma categoria for selecionada, um filtro será aplicado e apenas os produtos naquela categoria aparecerão. Os produtos serão mostrados em cards pequenos, com uma imagem principal, um nome e o preço, além de um overlay na imagem quanto a disponibilidade daquele produto. O clique em um card abre a tela Produto
   
- Produto - tela do produto contendo uma galeria daquele produto em específico, seu nome, preço, disponibilidade, estoque, quantidade selecionada, formas de entrega, detalhes, variantes do produto (se houver) e categorias, além do botão de compra, disponível quando a loja estiver aberta e o produto disponível. Esse botão pode variar de acordo com o status do produto, se tornando um botão "encomenda". De qualquer forma, o clique no botão adiciona a quantidade selecionada daquele produto ao carrinho


- Carrinho - o carrinho inclui todos os produtos adicionados pelo cliente durante sua sessão. Ele está disponível antes mesmo do login, mas apenas habilita a efetivação do pedido para usuários logados. Os produtos aparecem em cards horizontais, com detalhes sobre sua adição, bem como a possibilidade de editar a quantidade selecionada e remover o produto do carrinho. O botão para fechar pedido levará para o login em caso de usuário visitante. Caso o login já esteja ok, a tela acumulará a seleção para a forma de entrega e, posteriormente, a de pagamento, caso o pedido não dependa da aprovação manual. Os eventos cadastrados em que um pedido pode ser entregue aparecerão aqui, além da opção de cadastrar um endereço de entrega se isso for uma possibilidade para todos os produtos que estiverem no carrinho. A finalização de uma compra ou envio dela para aprovação levará o usuário para a tela de perfil, na parte de pedidos realizados


- Login - tela simples para login de usuários. É a mesma para administradores, e o modo de login varia de acordo com as credenciais inseridas. O normal é que seja incluído um email e senha, mas talvez haja o cadastro e login por CPF (a definir). A tela de login também se liga com a tela de criação do usuário. Após efetuar login, o site vai para a tela em que estava antes dela, com a sessão alterada para um usuário cadastrado


- Criar conta - tela para cadastro de usuários (compradores). As informações a serem fornecidas (além das especificadas no projeto) ainda serão definidas. Aqui, algum mecanismo de prevenção de spam e DDoS será incluído, além da necessidade de confirmação de email para efetivação da conta e habilitação do login


- Gerenciamento - tela acessível apenas pela administração. Contém um menu de navegação para telas de gerenciamento da loja, dos pedidos feitos, das mensagens recebidas e dos perfis dos clientes cadastrados. Os elementos serão carregados nessa tela de acordo com a seleção nesse menu. Aqui estarão funcionalidades como cadastro de novos produtos e edição de estoque, cadastro de eventos em que a retirada estará disponível, ferramentas para visualização dos pedidos, separando os pendentes dos efetivados e concluídos, bem como ferramentas de moderação de usuários e criação de novas contas administrativas


- Perfil do usuário - tela para usuários (clientes) cadastrados. Possui seus dados de cadastro com opções de alteração de determinadas informações, uma lista dos pedidos feitos e seus status, incluindo o botão Pagar para os pedidos que foram posteriormente aprovados pela administração, e uma página para chat com usuários administradores, mantendo históricos de mensagens enviadas por cada dia. A exclusão de conta pode ser feita aqui na aba de dados.


O logout de um usuário em qualquer situação o levará para a tela inicial.


