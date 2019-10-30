<script>


function presentModal() {
  // create the modal with the `modal-page` component
  const modalElement = document.createElement('ion-modal');
  modalElement.component = 'modal-page';

  // present the modal
  document.body.appendChild(modalElement);
  return modalElement.present();
}

async function presentToast() {
 const toast = document.createElement('ion-toast');
  toast.message = 'Your settings have been saved.';
  toast.duration = 2000;

  document.body.appendChild(toast);
  return toast.present();
}

async function presentActionSheet() {

  const actionSheet = document.createElement('ion-action-sheet');

  actionSheet.header = "Albums";
  actionSheet.buttons = [{
    text: 'Delete',
    role: 'destructive',
    icon: 'trash',
    handler: () => {
      console.log('Delete clicked');
    }
  }, {
    text: 'Share',
    icon: 'share',
    handler: () => {
      console.log('Share clicked');
    }
  }, {
    text: 'Play (open modal)',
    icon: 'arrow-dropright-circle',
    handler: () => {
      console.log('Play clicked');
    }
  }, {
    text: 'Favorite',
    icon: 'heart',
    handler: () => {
      console.log('Favorite clicked');
    }
  }, {
    text: 'Cancel',
    icon: 'close',
    role: 'cancel',
    handler: () => {
      console.log('Cancel clicked');
    }
  }];
  document.body.appendChild(actionSheet);
  return actionSheet.present();
}

async function presentAlert() {
const alert = document.createElement('ion-alert');
  alert.header = 'Alert';
  alert.subHeader = 'Subtitle';
  alert.message = 'This is an alert message.';
  alert.buttons = ['OK'];

  document.body.appendChild(alert);
  return alert.present();
}

async function presentMenu() {
	const menuCtrl = document.querySelector('ion-menu-controller');

 menuCtrl.enable(true, 'first');
}



</script>

<style>
	h1, figure, p {
		text-align: center;
		margin: 0 auto;
	}

	h1 {
		font-size: 2.8em;
		text-transform: uppercase;
		font-weight: 700;
		margin: 0 0 0.5em 0;
	}

	figure {
		margin: 0 0 1em 0;
	}

	img {
		width: 100%;
		max-width: 400px;
		margin: 0 0 1em 0;
	}

	p {
		margin: 1em auto;
	}

	@media (min-width: 480px) {
		h1 {
			font-size: 4em;
		}
	}
</style>
 

<svelte:head>
	<title>Sapper project template</title>
</svelte:head>


	<h1>Great success!</h1>
<ion-icon name="arrow-dropleft-circle"></ion-icon>

<ion-input value="custom"></ion-input>
<ion-avatar>
  <img src="https://gravatar.com/avatar/dba6bae8c566f9d4041fb9cd9ada7741?d=identicon&f=y">
</ion-avatar>

<ion-menu side="start" menu-id="first">
    <ion-header>
      <ion-toolbar color="primary">
        <ion-title>Start Menu</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content>
      <ion-list>
        <ion-item>Menu Item</ion-item>
        <ion-item>Menu Item</ion-item>
        <ion-item>Menu Item</ion-item>
        <ion-item>Menu Item</ion-item>
        <ion-item>Menu Item</ion-item>
      </ion-list>
    </ion-content>
  </ion-menu>

<ion-menu-controller></ion-menu-controller>

	<figure>
		<img alt='Borat' src='great-success.png'>
		<figcaption>HIGH FIVE!</figcaption>
	</figure>

		<!-- Cool thing, the Ionic CSS utilities could be used too -->

			<h1>Basic usage</h1>
			<!-- We add an ion-button with an onclick event -->
			<ion-button on:click="{presentToast}" >Toast</ion-button>
			<ion-button on:click="{presentActionSheet}" >ActionSheet</ion-button>
			<ion-button on:click="{presentAlert}" >PresentAlert</ion-button>
			<ion-button on:click="{presentMenu}" >PresentMenu</ion-button>
				<ion-button on:click="{presentModal}" >presentModal</ion-button>
			



					
	<ion-badge color="primary">11</ion-badge>

	<ion-card>
	<ion-card-header>
		<ion-card-subtitle>Card Subtitle</ion-card-subtitle>
		<ion-card-title>Card Title</ion-card-title>
	</ion-card-header>

	<ion-card-content>
		Keep close to Nature's heart... and break clear away, once in awhile,
		and climb a mountain or spend a week in the woods. Wash your spirit clean.
	</ion-card-content>
	</ion-card>

	<ion-checkbox color="primary"></ion-checkbox>

	<ion-item>
	<ion-label>Disabled</ion-label>
	<ion-datetime id="dynamicDisabled" display-format="MM DD YY" disabled value="1994-12-15"></ion-datetime>
	</ion-item>

	<ion-fab vertical="bottom" horizontal="start">
		<ion-fab-button>
		<ion-icon name="arrow-dropup"></ion-icon>
		</ion-fab-button>
	</ion-fab>

	<ion-list>
	<ion-list-header>Single Selection</ion-list-header>

	<ion-item>
		<ion-label>Gender</ion-label>
		<ion-select placeholder="Select One">
		<ion-select-option value="f">Female</ion-select-option>
		<ion-select-option value="m">Male</ion-select-option>
		</ion-select>
	</ion-item>

	<ion-item>
		<ion-label>Hair Color</ion-label>
		<ion-select value="brown" ok-text="Okay" cancel-text="Dismiss">
		<ion-select-option value="brown">Brown</ion-select-option>
		<ion-select-option value="blonde">Blonde</ion-select-option>
		<ion-select-option value="black">Black</ion-select-option>
		<ion-select-option value="red">Red</ion-select-option>
		</ion-select>
	</ion-item>

	</ion-list>



<ion-grid>
  <ion-row>
    <ion-col>
      ion-col
    </ion-col>
    <ion-col>
      ion-col
    </ion-col>
    <ion-col>
      ion-col
    </ion-col>
    <ion-col>
      ion-col
    </ion-col>
  </ion-row>

  <ion-row>
    <ion-col size="6">
      ion-col [size="6"]
    </ion-col>
    <ion-col>
      ion-col
    </ion-col>
    <ion-col>
      ion-col
    </ion-col>
  </ion-row>

  <ion-row>
    <ion-col size="3">
      ion-col [size="3"]
    </ion-col>
    <ion-col>
      ion-col
    </ion-col>
    <ion-col size="3">
      ion-col [size="3"]
    </ion-col>
  </ion-row>

  <ion-row>
    <ion-col size="3">
      ion-col [size="3"]
    </ion-col>
    <ion-col size="3" offset="3">
      ion-col [size="3"] [offset="3"]
    </ion-col>
  </ion-row>

  <ion-row>
    <ion-col>
      ion-col
    </ion-col>
    <ion-col>
      ion-col
      <br>#
    </ion-col>
    <ion-col>
      ion-col
      <br>#
      <br>#
    </ion-col>
    <ion-col>
      ion-col
      <br>#
      <br>#
      <br>#
    </ion-col>
  </ion-row>

  <ion-row>
    <ion-col align-self-start>
      ion-col [start]
    </ion-col>
    <ion-col align-self-center>
      ion-col [center]
    </ion-col>
    <ion-col align-self-end>
      ion-col [end]
    </ion-col>
    <ion-col>
      ion-col
      <br>#
      <br>#
    </ion-col>
  </ion-row>

  <ion-row align-items-start>
    <ion-col>
      [start] ion-col
    </ion-col>
    <ion-col>
      [start] ion-col
    </ion-col>
    <ion-col align-self-end>
      [start] ion-col [end]
    </ion-col>
    <ion-col>
      ion-col
      <br>#
      <br>#
    </ion-col>
  </ion-row>

  <ion-row align-items-center>
    <ion-col>
      [center] ion-col
    </ion-col>
    <ion-col>
      [center] ion-col
    </ion-col>
    <ion-col>
      [center] ion-col
    </ion-col>
    <ion-col>
      ion-col
      <br>#
      <br>#
    </ion-col>
  </ion-row>

  <ion-row align-items-end>
    <ion-col>
      [end] ion-col
    </ion-col>
    <ion-col align-self-start>
      [end] ion-col [start]
    </ion-col>
    <ion-col>
      [end] ion-col
    </ion-col>
    <ion-col>
      ion-col
      <br>#
      <br>#
    </ion-col>
  </ion-row>

  <ion-row>
    <ion-col size="12" size-sm>
      ion-col [size="12"] [size-sm]
    </ion-col>
    <ion-col size="12" size-sm>
      ion-col [size="12"] [size-sm]
    </ion-col>
    <ion-col size="12" size-sm>
      ion-col [size="12"] [size-sm]
    </ion-col>
    <ion-col size="12" size-sm>
      ion-col [size="12"] [size-sm]
    </ion-col>
  </ion-row>

  <ion-row>
    <ion-col size="12" size-md>
      ion-col [size="12"] [size-md]
    </ion-col>
    <ion-col size="12" size-md>
      ion-col [size="12"] [size-md]
    </ion-col>
    <ion-col size="12" size-md>
      ion-col [size="12"] [size-md]
    </ion-col>
    <ion-col size="12" size-md>
      ion-col [size="12"] [size-md]
    </ion-col>
  </ion-row>

  <ion-row>
    <ion-col size="6" size-lg offset="3">
      ion-col [size="6"] [size-lg] [offset="3"]
    </ion-col>
    <ion-col size="3" size-lg>
      ion-col [size="3"] [size-lg]
    </ion-col>
  </ion-row>
</ion-grid>

	<p><strong>Try editing this file (src/routes/index.svelte) to test live reloading.</strong></p>

