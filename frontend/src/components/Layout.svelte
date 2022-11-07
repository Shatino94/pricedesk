<script>

    import {
      Header,
      HeaderNav,
      HeaderNavItem,
      HeaderNavMenu,
      SkipToContent,
      Content,
      Grid,
      Row,
      Column,
    } from "carbon-components-svelte";
  
    let isSideNavOpen = false;
    import '../styles/index.scss';
  </script>
  
  <Header  platformName="PriceDesk" bind:isSideNavOpen>
    <svelte:fragment slot="skip-to-content">
      <SkipToContent />
    </svelte:fragment>
    <HeaderNav>
      <HeaderNavItem href="/" text="FAQ" />
  
      <HeaderNavMenu text="Currency">
        <HeaderNavItem href="/" text="USD" />
        <HeaderNavItem href="/" text="LRD" />
        
      </HeaderNavMenu>

      <HeaderNavMenu text="Locations">
        <HeaderNavItem href="/" text="Red Light" />
        <HeaderNavItem href="/" text="Waterside" />
        <HeaderNavItem href="/" text="Duala" />
        
      </HeaderNavMenu>
    </HeaderNav>
  </Header>
  
  <Content>
    <Grid>
      <Row>
        <Column>
        <slot/>
        </Column>
      </Row>
    </Grid>
  </Content>
  