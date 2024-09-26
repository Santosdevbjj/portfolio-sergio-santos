
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Portfólio de Sérgio Santos</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background-color: #333;
            color: #fff;
            padding: 10px 0;
            text-align: center;
        }
        header h1 {
            margin: 0;
            font-size: 2.5em;
        }
        section {
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        .about {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            align-items: center;
            text-align: center;
        }
        .about img {
            border-radius: 50%;
            width: 200px;
            height: 200px;
            object-fit: cover;
            margin-right: 20px;
        }
        .about div {
            max-width: 800px;
        }
        .experience {
            margin-top: 40px;
        }
        .container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
        }
        .card {
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            margin: 20px;
            padding: 20px;
            width: 300px;
            text-align: center;
        }
        .card h3 {
            margin-bottom: 15px;
        }
        .card p {
            color: #555;
        }
        footer {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 10px 0;
            margin-top: 20px;
        }
        @media (max-width: 768px) {
            .about {
                flex-direction: column;
            }
            .about img {
                margin: 0 0 20px 0;
            }
        }
    </style>
</head>
<body>

<header>
    <h1>Portfólio de Sérgio Santos</h1>
</header>

<section class="about">
    <img src="sua-foto.jpg" alt="Foto de Sérgio Santos">
    <div>
        <h2>Sobre Mim</h2>
        <p>Sou um profissional com sólida carreira na área de Tecnologia da Informação, e também tenho experiência no campo do Direito. Possuo ampla vivência em análise, programação e desenvolvimento de sistemas, com destacada atuação em projetos de tecnologia voltados para o setor bancário. Competente na instalação, configuração e manutenção de sistemas operacionais Windows e dispositivos de rede. Retornando ao mercado após um período afastado, estou com disposição para enfrentar novos desafios, aprimorar conhecimentos e aplicar soluções inovadoras.</p>
    </div>
</section>

<section class="experience">
    <h2>Experiência Profissional</h2>
    <p>Tenho vasta experiência na área de Tecnologia da Informação, com um histórico de sucesso em:</p>
    <ul>
        <li>Desenvolvimento de soluções para processamento bancário.</li>
        <li>Administração e configuração de redes de computadores com mais de 500 usuários.</li>
        <li>Instalação e manutenção de sistemas operacionais Windows NT/2000.</li>
        <li>Elaboração de documentação técnica e manuais de sistemas.</li>
        <li>Trabalho com normas de segurança em servidores Windows.</li>
    </ul>
</section>

<section>
    <h2>Minhas Habilidades</h2>
    <div class="container">
        <div class="card">
            <h3>Desenvolvimento de Sistemas</h3>
            <p>Experiência com análise, programação e desenvolvimento de sistemas, incluindo soluções para o setor bancário.</p>
        </div>
        <div class="card">
            <h3>Configuração de Redes</h3>
            <p>Ampla vivência na configuração de dispositivos de rede e administração de redes com mais de 500 usuários.</p>
        </div>
        <div class="card">
            <h3>Windows NT/2000</h3>
            <p>Instalação, configuração e manutenção de sistemas operacionais Windows NT/2000 PRO e servidores.</p>
        </div>
    </div>
</section>

<section>
    <h2>Qualificações Técnicas</h2>
    <ul>
        <li>Microsoft Visual Basic 6.0</li>
        <li>Sistemas Operacionais Windows (instalação, configuração e suporte)</li>
        <li>Instalação e configuração de dispositivos de rede e periféricos</li>
        <li>Desenvolvimento de sistemas para o setor bancário</li>
        <li>Elaboração de documentação técnica e manuais de usuário</li>
        <li>Administração de servidores Windows e gerenciamento de permissões de rede</li>
        <li>Suporte técnico a usuários finais e clientes internos</li>
        <li>Resolução de problemas de hardware e software</li>
    </ul>
</section>

<footer>
    <p>© 2024 Sérgio Santos. Todos os direitos reservados.</p>
</footer>

</body>
</html>
