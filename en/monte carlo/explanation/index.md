# Monte Carlo

It is possible to approximate an integral by using random numbers. In the following video the main principles of Monte Carlo simulation are explained.

![embed](https://www.youtube.com/embed/7ESK5SaP-bc)

We will be applying Monte Carlo simulation to determine the integral area of a function between two limits. The following video explains the process:

![embed](https://api.eu.kaltura.com/p/120/sp/12000/embedIframeJs/uiconf_id/23449960/partner_id/120?iframeembed=true&playerId=kaltura_player&entry_id=0_t25rc4ue&flashvars[streamerType]=auto&amp;flashvars[localizationCode]=en_US&amp;flashvars[leadWithHTML5]=true&amp;flashvars[sideBarContainer.plugin]=true&amp;flashvars[sideBarContainer.position]=left&amp;flashvars[sideBarContainer.clickToClose]=true&amp;flashvars[chapters.plugin]=true&amp;flashvars[chapters.layout]=vertical&amp;flashvars[chapters.thumbnailRotator]=false&amp;flashvars[streamSelector.plugin]=true&amp;flashvars[EmbedPlayer.SpinnerTarget]=videoHolder&amp;flashvars[dualScreen.plugin]=true&amp;flashvars[hotspots.plugin]=1&amp;flashvars[Kaltura.addCrossoriginToIframe]=true&amp;&wid=0_xccg5bs5)


To summarize, numerical integration with Monte Carlo simulation can be defined as follows:

1.  Define a rectangle that surrounds the integral area

    Define an area (often times a rectangle) that surrounds the integral area. So you have to choose a $$x_{min}$$, $$x_{max}$$, $$y_{min}$$ and $$y_{max}$$ such that:

      - $$x_{min} \leq a$$ and $$x_{max} \geq b​$$

      - for $$a \leq x \leq b$$ : $$y_{min} \leq f(x)  \leq y_{max}$$

    Choose the tightest rectangle with $$x_{min} = a$$ and $$x_{max} = b$$.

2.  Generate random points within the rectangle

    Generate a large number of random numbers $$(x_i, y_i)$$ in the rectangle that surrounds the integral area and verify for each point whether it lies 'within' the integral area ('good') or not ('wrong'). Keep track of the fraction of points within the integral area: $$f_{good}​$$.

3.  Determine the integral

    The integral is the fraction of points generated within the graph times the total surface of the rectangle ('box').
    In case of a rectangle the integral is given by:

    $$
        \int_a^b f(x)~dx = f_{good}~~\cdot~(x_{max}-x_{min})\cdot(y_{max}-y_{min})
    $$

## Example

It is known that the equation $$sin(x)$$ is enclosed on the domain $$0 < x < \pi$$ between 0 and 1. So, we defined a box around the integral area and generated 2000 random points, of which 63.15% (1263/2000) appeared to be within the integral area. The approximation that we've made of the integral using these 2000 points is subsequently: 0.6315$$\pi \approx 1.984​$$. When this method is implemented correctly, we can effortlessly generate 1 million points instead of 2000.

![](../../../assets/MonteCarloExample.png)
