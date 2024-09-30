# Loja Lullaboo (e Artist's Alley)
## SCC0219 - 2024.2

Aluna: Gabriela Bacarin Marcondes #10873351

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

- Possibilidade de definir individualmente as formas de entrega disponíveis para cada produto, inclusive um número mínimo de produtos iguais para elegibilidade de envio

- Possibilidade de moderação de contas de usuários, inclusive restringir compras, restringir mensagens ou excluir a conta

- Possibilidade de rejeitar pedidos em qualquer momento desde que combinado com o comprador, facilitando possível devolução de dinheiro

![image](https://github.com/user-attachments/assets/ca73b6cf-111f-43b7-9207-35ee0715e209)
