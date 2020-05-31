<script>

  import { isActive, url } from '@sveltech/routify';

  // UI controls

  import Icon from '../../UI/Icon.svelte';
  import Button from '../../UI/Button.svelte';
  import ButtonToolbar from '../../UI/ButtonToolbar.svelte';
  import NavBar from '../../UI/Navbar.svelte';

  import ContentArea from '../../UI/ContentArea.svelte';

  import Toolbar from '../../UI/Toolbar.svelte';
  import ToolbarGroup from '../../UI/ToolbarGroup.svelte';
  import ToolbarItem from '../../UI/ToolbarItem.svelte';
  import ToolbarTitle from '../../UI/ToolbarTitle.svelte';

</script>

<NavBar borderPosition="bottom" background="alt">
    <Toolbar>
        <ToolbarGroup align="left">
            <ToolbarItem>
                <Button icon="chevron-left" variant="ghost" href="{$url("/")}">Back</Button>
            </ToolbarItem>
        </ToolbarGroup>
        <ToolbarGroup align="center">
            <ToolbarItem>
                <ToolbarTitle>Detail</ToolbarTitle>
            </ToolbarItem>
        </ToolbarGroup>
        <ToolbarGroup align="right">
            <ToolbarItem>
            </ToolbarItem>
        </ToolbarGroup>
    </Toolbar>
</NavBar>

<ContentArea>
  <div class="u-spacer">
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
  </div>
</ContentArea>
