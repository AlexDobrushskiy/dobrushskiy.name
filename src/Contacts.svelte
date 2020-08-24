<script>
  import MailIcon from '../assets/mail_icon.svg';
  import PhoneIcon from '../assets/phone_icon.svg';
  import Social from './Header/Social.svelte';
</script>
<style lang="scss">

  $left-shift: 68px;
  .main {
    min-height: 777px;
    @media (max-width: 768px) {
      min-height: 0;
    }
    background-position: 600px -80px;
    background-repeat: no-repeat;
    background-image: url("/images/bg4.jpg")
    /*background-size: calc(100% - 600px);*/
  }

  h1 {
    margin-left: $left-shift;
    @media (max-width: 768px) {
      margin-left: 20px;
    }

    margin-top: 20px;
    font-size: 48px;
    color: var(--light-navy);
    margin-bottom: 0;
  }

  p {
    margin-left: $left-shift;

    margin-top: 50px;
    @media (max-width: 768px) {
      margin-top: 20px;
      margin-left: 20px;
    }
    max-width: 600px;
    color: var(--black);
    font-size: 18px;
    font-weight: 300;
  }

  .signature {
    display: flex;
    @media (max-width: 768px) {
      flex-direction: column;
    }
    margin-left: $left-shift;
    @media (max-width: 768px) {
      margin-left: 20px;
    }

    margin-top: 20px;
    margin-bottom: 0;

    h3 {
      font-size: 30px;
      color: var(--light-navy);
      margin-right: 50px;
      font-style: italic;
    }
  }

  .contact {
    margin-left: $left-shift;
    @media (max-width: 768px) {
      margin-left: 20px;
    }

    margin-top: 15px;
    font-size: 18px;
    font-weight: 300;

    img {
      margin-right: 15px;
      margin-bottom: -5px;
    }
  }

  .signature + .contact {
    margin-top: 30px;
  }

  a {
    color: inherit;
    text-decoration: none;
    &:hover {
      text-decoration:none;
    }
  }
  .contact-me {
    margin-left: $left-shift;
    @media (max-width: 768px) {
      margin-left: 20px;
    }

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
    text-decoration: none;
  }
</style>

<div class="main" id="id-contacts">
  <h1>Contacts</h1>
  <p>Alex is always happy to discuss a new opportunities. Even he is occupied with another project at the moment - he can consult you regarding your project or advice someone to help with the development.
    <br/>
    <br/>If you have a startup or just an idea and need a technical co-founder/CTO/technical partner - you definetely should have a chat with him.</p>
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
  <a href="mailto:a.dobrushskiy@gmail.com?subject=[dobrushskiy.name] Hello" target="_blank">
    <div class="contact-me">
      Conctact Alex
    </div>
  </a>
</div>