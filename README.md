<h1>HDC Eventos - Versão Eficaz</h1>

<h2>Descrição do Projeto</h2>
<p>Este projeto foi desenvolvido como parte de um processo seletivo, com o objetivo de avaliar conhecimentos em <strong>Laravel</strong>, <strong>Blade</strong>, <strong>HTML</strong>, <strong>CSS</strong>, <strong>JavaScript</strong>, boas práticas de código, tratamento de erros, GitHub e capacidade técnica e criativa para implementar novas funcionalidades em cima de uma base existente.</p>
<p>A aplicação permite o cadastro e login de usuários, criação, edição e exclusão de eventos, inscrição de usuários nos eventos, além de exibir notificações e um dashboard personalizado.</p>

<h2>Funcionalidades</h2>

<h3>Padrão da Base (Projeto Curso Hora de Codar):</h3>

<ul>
  <li>Cadastro de usuários e autenticação (login/logout).</li>
  <li>Criação, edição e exclusão de eventos.</li>
  <li>Inscrição e saída de eventos pelos usuários.</li>
  <li>Visualização de todos os eventos com filtro por título.</li>
  <li>Dashboard do usuário com eventos cadastrados e eventos que participa.</li>
</ul>

<h3>Funcionalidades Implementadas (Solicitados no Projeto):</h3>

<ul>
  <li>Diferenciação de <strong>níveis de usuários</strong> (admin e usuário comum) para permissões específicas:
    <ul>
      <li>Admin pode criar, editar e excluir eventos.</li>
      <li>Usuários comuns podem se inscrever em eventos.</li>
    </ul>
  </li>
  <li>Retorno dos dados dos eventos via <strong>API</strong> (rota <code>/api/events</code> disponível).</li>
  <li>Notificações em tempo real para:
    <ul>
      <li>Novos eventos (exceto para o criador do evento)</li>
      <li>Atualização de eventos (para participantes, exceto o criador)</li>
      <li>Cancelamento de eventos (para participantes, exceto o criador)</li>
      <li>Inscrição e saída de eventos</li>
    </ul>
  </li>
  <li>Responsividade completa para desktop e mobile.</li>
  <li>Páginas referentes à conta do usuário: editar dados, alterar senha.</li>
</ul>

<h2>Tecnologias Utilizadas</h2>
<ul>
  <li><strong>Backend:</strong> Laravel 10</li>
  <li><strong>Frontend:</strong> Blade, HTML, CSS, JavaScript</li>
  <li><strong>Banco de Dados:</strong> MySQL (padrão Laravel)</li>
  <li><strong>Controle de Versão:</strong> Git + GitHub</li>
</ul>

<h2>Estrutura do Projeto</h2>
<pre>
app/
├─ Http/
│  ├─ Controllers/
│  │  ├─ EventController.php
│  │  ├─ AccountController.php
│  │  └─ NotificationController.php
│  └─ Middleware/
│     └─ Admin.php
├─ Models/
│  ├─ Event.php
│  ├─ User.php
│  └─ Notification.php
database/
├─ migrations/
├─ seeders/
resources/
├─ views/
│  ├─ events/
│  ├─ account/
│  └─ layouts/
public/
├─ img/
│  ├─ events/
│  └─ profiles/
</pre>

<h2>Instalação e Configuração</h2>
<ol>
  <li>Clone o repositório:
    <pre><code>git clone https://github.com/zedourado/projeto-hdceventos-eficaz.git
cd projeto-hdceventos-eficaz</code></pre>
  </li>
  <li>Instale as dependências:
    <pre><code>composer install
npm install
npm run dev</code></pre>
  </li>
  <li>Configure o <code>.env</code> com seu banco de dados e chave de aplicação:
    <pre><code>cp .env.example .env
php artisan key:generate</code></pre>
  </li>
  <li>Instale/Execute o XAMPP/Laragon: https://www.apachefriends.org/pt_br/download.html
  </li>
  <li>Crie o banco de dados:
    <pre>
      <code>
        CREATE DATABASE laravel
        CHARACTER SET utf8mb4
        COLLATE utf8mb4_unicode_ci;
      </code>
    </pre>
  </li>
  </li>
    <li>Execute o Seeder para criar o Usuário Admin:
    <pre><code>php artisan db:seed --class=AdminSeeder</code></pre>
    <span><strong>User:</strong> admin@hdcevents.com -- <strong>Senha:</strong> password </span>
  </li>
  <li>Execute as migrations:
    <pre><code>php artisan migrate</code></pre>
  </li>
  <li>Inicie o servidor:
    <pre><code>php artisan serve</code></pre>
    <p>Acesse a aplicação em: <a href="http://127.0.0.1:8000">http://127.0.0.1:8000</a></p>
  </li>
</ol>

<h2>Demonstração das Funcionalidades</h2>
<ul>
  <li><strong>Eventos:</strong> Criação, edição, exclusão e listagem de eventos.</li>
  <li><strong>Inscrição em Eventos:</strong> Usuários podem se inscrever e sair de eventos.</li>
  <li><strong>Dashboard do Usuário:</strong> Eventos cadastrados e eventos que participa.</li>
  <li><strong>Notificações:</strong> Sistema de notificações em tempo real com badge e marcação de notificações lidas.</li>
  <li><strong>Responsividade:</strong> Funciona em diferentes tamanhos de tela.</li>
  <li><strong>API:</strong> Retorno de eventos via rota <code>/api/events</code>.</li>
</ul>

<h2>Autor</h2>
<p><strong>José Roberto Dourado Junior</strong></p>
<ul>
  <li>GitHub: <a href="https://github.com/zedourado">https://github.com/zedourado</a></li>
  <li>Projeto desenvolvido para apresentação em processo seletivo.</li>
</ul>
