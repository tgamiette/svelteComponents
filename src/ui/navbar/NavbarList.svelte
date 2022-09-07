<script>
    import Navbar from './Navbar.svelte';
    import CodeDisplay from '../CodeDisplay/CodeDisplay.svelte';

  </script>

  <h2>Navbar</h2>
  <section class="navbar">
      <Navbar
        logo="src/assets/svelte.svg"
        items= {[ {link:"", text:"Nouveautés"}, {link:"", text:"Vêtements"}, {link:"", text:"Chaussures"}, {link:"", text:"Accessoires"}, {link:"", text:"Seconde main"} ]}
        links= {[ {link:"", text:"Mon compte"}, {link:"", text:"S'inscrire"} ]}
      />

      <CodeDisplay tabs={[
        {label: 'App.svelte',
        value: `
          <script>
            import Navbar from './Navbar.svelte';
          </script>
          <Navbar
                logo="src/assets/svelte.svg"
                items= {[ {link:"", text:"Nouveautés"}, {link:"", text:"Vêtements"}, {link:"", text:"Chaussures"}, {link:"", text:"Accessoires"}, {link:"", text:"Seconde main"} ]}
                links= {[ {link:"", text:"Mon compte"}, {link:"", text:"S'inscrire"} ]}
            />`
        },{
          label:'Navbar.svelte',
          value: `
            <script>
                export let logo = "";
                export let items = [
                    {link: "", text: ""}
                ];
                export let links = [
                    {link: "", text: ""}
                ];

            </script>

            <div class="navbar">
            <figure class="logo">
                <img src={ logo } alt="Logo"/>
            </figure>

                <ul class="nav-items menus">
                    {#each items as item}
                        <li>
                            <a href={ item.link }>{ item.text }</a>
                        </li>
                    {/each}
                </ul>

                <ul class="nav-items links">
                    {#each links as link}
                    <li>
                        <a href={ link.link }>{ link.text }</a>
                    </li>
                    {/each}
                </ul>
            </div>

            <style>
            .navbar {
                width: 100%;
                height: 65px;
                color: #2e2d2d;
                display: flex;
                flex-direction: row;
                justify-content: space-between;
                font-size: 14px;
                font-family: 'Franklin Gothic Medium';
            }

            .logo {
                max-width: 200px;
                cursor: pointer;
            }

            img {
                width: 100%;
                height: auto;
            }

            .nav-items {
                display: flex;
                justify-content: center;
                height: 100%;
                align-items: center;
                list-style-type: none;
            }

            a {
                text-decoration: none;
                color: #2e2d2d;
                padding: 0 20px;
                text-transform: uppercase;
                letter-spacing: 1px;
            }

            .menus a {
                font-size: 14px;
            }

            .menus a:hover {
                font-weight: bold;
            }

            .links a {
                font-size: 12px;
            }

            .links a:hover {
                text-decoration: underline;
                font-weight: normal;
            }
            </style>
          `
        }]} />


  </section>

  <style>

    .productCard{
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-gap: 50px;
      width: 100%;
    }

  </style>
