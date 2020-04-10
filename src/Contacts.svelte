<script>
  import BgImage from '../assets/bg4.jpg';
  import MailIcon from '../assets/mail_icon.svg';
  import PhoneIcon from '../assets/phone_icon.svg';
  import Social from './Header/Social.svelte';
</script>
<style lang="scss">
  $left-shift: 68px;
  .main {
    min-height: 777px;
    background-position: 600px -80px;
    background-repeat: no-repeat;
    /*background-size: calc(100% - 600px);*/
  }

  h1 {
    margin-left: $left-shift;
    margin-top: 20px;
    font-size: 48px;
    color: var(--light-navy);
    margin-bottom: 0;
  }

  p {
    margin-left: $left-shift;
    margin-top: 50px;
    max-width: 600px;
    color: var(--black);
    font-size: 18px;
    font-weight: 300;
  }

  .signature {
    display: flex;
    margin-left: $left-shift;
    margin-top: 20px;
    margin-bottom: 0;

    h3 {
      font-size: 32px;
      color: var(--light-navy);
      margin-right: 50px;
      /*margin-bottom: 20px;*/
    }
  }
  .contact {
    margin-left: $left-shift;
    margin-top: 15px;
    font-size: 18px;
    font-weight: 300;
    img {
      margin-right: 15px;
      margin-bottom: -5px;
    }
  }
  .signature+.contact {
    margin-top: 30px;
  }
  .contact-me {
    margin-left: $left-shift;
    border-radius: 100px;
    height: 71px;
    background-color: var(--text-color-2);
    color: var(--white);
    font-size: 24px;
    font-weight: bold;
    text-align: center;
    width: 281px;
    margin-top: 49px;
    line-height: 71px;
    cursor: pointer;
  }
</style>

<div class="main" style="background-image: url({BgImage})" id="id-contacts">
  <h1>Contacts</h1>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla ut mattis eros, a sagittis risus. Nullam feugiat,
    risus eu vehicula dictum, enim arcu posuere sapien, in sodales enim neque eget elit. Nam fermentum eu metus id
    vehicula. Aliquam eleifend augue a semper lacinia. Maecenas eleifend lacus magna, a dignissim nisi laoreet
    sollicitudin. Quisque congue eu lectus tincidunt dignissim. Nunc at dolor eros. Pellentesque consequat mauris ac mi
    volutpat egestas. Nulla facilisi</p>
  <div class="signature">
    <h3>Alex Dobrushskiy</h3>
    <Social/>
  </div>
  <div class="contact">
    <img src={PhoneIcon} alt="phone icon"> 7 920 039 32 89
  </div>
  <div class="contact">
    <img src={MailIcon} alt="mail icon"> a.dobrushskiy@gmail.com
  </div>
  <div class="contact-me">
    Conctact with me
  </div>
</div>