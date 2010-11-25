# Front-end Admin bar

---------------------------------------

This is a XSLT utility for Symphony CMS that adds a simple admin bar in the top of the site when logged in as a developer/author, displaying options like 'Logout' or 'Back to admin'.

---------------------------------------

## Info
- Version:	0.1
- Date:		24-119-2010
- Author:	João Barbosa
- E-mail:	<joao.ofb@gmail.com>
- Website:	<www.joaootavio.com.br>

---------------------------------------

## Sample CSS Code

<https://gist.github.com/714098>

---------------------------------------

## Usage

Add the <code>admin-bar.xsl</code> file to your <code>/workspace/utilities</code> folder.

On your <code>master.xsl</code> (or an specific page you want to use it), import the XSL file...

<code><xsl:import href="../utilities/admin-bar.xsl"/></code>

... and call the template right after your <code><body></body> tag:

<code>
	<xsl:call-template name="front-admin-bar">
		<xsl:with-param name="logged-label" select="Logged in as: " />
		<xsl:with-param name="logged-label" select="Back to admin" />
		<xsl:with-param name="logged-label" select="Logout" />
	</xsl:call-template>
</code>

---------------------------------------

## Parameters

- **logged-label**: text that precedes username link  
*Optional. Default Value: 'Logged in as: '*
- **admin-link**: text for the administration link  
*Optional. Default Value: 'Back to admin'*
- **logout-link**: text for the logout link  
*Optional. Default Value: 'Logout'*
