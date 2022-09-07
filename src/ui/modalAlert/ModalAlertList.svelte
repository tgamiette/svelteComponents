<script>
    import CodeDisplay from '../CodeDisplay/CodeDisplay.svelte';
    import ModalAlert from "./ModalAlert.svelte";
  
  </script>
  
  <h2>Modal Alert</h2>
  <section class="modalAlert">
    <div class="exemple">
      <ModalAlert />
    </div>
      <CodeDisplay tabs={[
        {label: 'App.svelte',
        value: `
          <script>
            import ModalAlert from "./ModalAlert.svelte";
          </script>
  `
        },{
          label:'ModalAlert.svelte',
          value: `
  <script>
    export let buttonTitle = 'Delete'
    export let modalTitle = 'Are you absolutely sure?'
    export let modalDescription = 'This action cannot be undone. This will permanently delete your account and remove your data from our servers.'
    export let modalConfirmation = 'Yes, delete account'
    export let modalCancel = 'Cancel'

    let modalIsOpen = false
    const toggle = () => {
        modalIsOpen = !modalIsOpen
    }
  </script>
    <button on:click={ toggle }>
    { buttonTitle }
    </button>

    {#if modalIsOpen}
        <div class="modal-container" on:click={ toggle }>
            <div class="modal">
                <div class="modal__title">{ modalTitle }</div>
                <div class="modal__description">{ modalDescription }</div>
                <div class="modal__button">
                    <button class="modal__button-cancel" on:click={ toggle }>{ modalCancel }</button>
                    <button class="modal__button-confirmation" on:click={ toggle }>{ modalConfirmation }</button>
                </div>
            </div>
        </div>
    {/if}

    <style lang="scss">

        .modal-container {
            width: 100vw;
            height: 100vh;
            background-color: #80808070;
            position: fixed;
            display: flex;
            top: 0;
            bottom: 0;
            left: 0;
            right: 0;
        }

        .modal {
            margin: auto;
            width: 33%;
            background-color: white;
            border-radius: 8px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            padding: 16px;
            row-gap: 16px;

            &__title {
                font-weight: bold;
                font-size: 24px;
            }

            &__description {
                color: gray;
                font-size: 16px;
            }

            &__button {
                display: flex;
                justify-content: center;
                gap: 8px;

                &-cancel {
                    border-radius: 4px;
                    background-color: gray;
                }

                &-confirmation {
                    border-radius: 4px;
                    background-color: red;
                }
            }
        }
    </style>



  
          `
        }]} />
  
  
  </section>
  
  <style>
  
    .modalAlert{
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-gap: 50px;
      width: 100%;
    }
  
  </style>