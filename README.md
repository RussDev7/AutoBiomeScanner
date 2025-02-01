# AutoBiomeScanner - Moves around the map looking for stony_shore

1. First you need a Browser Extension for managing UserScripts[[1]][userscrips_faq] (skip if you already have one):  
   * Chrome: [Violentmonkey][chrome_violentmonkey] or [Tampermonkey][chrome_tampermonkey]
   * Firefox: [Greasemonkey][firefox_greasemonkey], [Tampermonkey][firefox_tampermonkey], or [Violentmonkey][firefox_violentmonkey]  
   * Opera: [Tampermonkey][opera_tampermonkey] or [Violentmonkey][opera_violentmonkey]
   * Brave: [Violentmonkey][chrome_violentmonkey] or [Tampermonkey][chrome_tampermonkey]
   * Edge: [Tampermonkey][edge_tampermonkey]  
   * Safari: ~[Tampermonkey][safari_tampermonkey]~ 
    
1. Install AutoBiomeScanner:  
  [![][greasyfork_icon]][greasyfork_url]

1. Open <a href="https://map.jacobsjo.eu/" target="_blank">map.jacobsjo.eu</a> in your __browser__ and zoom out as far out as possible.

1. Click the <kbd>🔎</kbd> button from the menu and select only the **Stony Shore** biome.

1. Click the ![StartButton](https://raw.githubusercontent.com/RussDev7/AutoBiomeScanner/refs/heads/main/images/startButtonHelp.png) button to begin scanning! 


![Screenshot](https://raw.githubusercontent.com/RussDev7/AutoBiomeScanner/refs/heads/main/images/autoBiomeScannerAction.gif)

----

### Why is this script needed?
Here is an example of a `stony_shore` biome being successfully found on my personal world.

![Screenshot](https://raw.githubusercontent.com/RussDev7/AutoBiomeScanner/refs/heads/main/images/shoresFound.png)

When using [terralith] along side [terratonic], you can find fairly quickly that `stony_shore` become near to none. The reason for this is because Terralith makes these biomes relatively tiny, then combine that with Terratonic's further smoothing mechanics, the stony_shore biome gets completely flattened over and eradicated. So this makes stony_shore biomes one of the rarest biomes under these two mods.

![Screenshot](https://raw.githubusercontent.com/RussDev7/AutoBiomeScanner/refs/heads/main/images/shoresInGame.png)

----

### How it works?
This script performs `canvas` click movements through javascript that follow a spiral type pattern. Each movement or "step" moves at half your windows height in all directions. This ensures a smooth transition throughout all **XY** movements.

After each step, the script then scans each `canvas` element for a specified color, and if none is found, deletes the `canvas` element and Illiterate through all remaining `canvas` elements before doing a new step.

![Screenshot](https://raw.githubusercontent.com/RussDev7/AutoBiomeScanner/refs/heads/main/images/autoBiomeScannerMath.png)

----

### Found a bug?
Find an issue? Feel free to submit a new [issues]. If you're not familiar with bug reports, please use the [discussions] tab instead.

----
#### DISCLAIMER

> THE SOFTWARE AND ALL INFORMATION HERE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
>
> By using any code or information provided here you are agreeing to all parts of the above Disclaimer.

<!-- links -->
  [userscrips_faq]: https://en.wikipedia.org/wiki/Userscript
  [greasyfork_icon]: https://user-images.githubusercontent.com/3372598/166113712-1bc3d654-1342-4f1e-9845-21c3b21524b1.png
  [terralith]: https://modrinth.com/datapack/terralith
  [terratonic]: https://modrinth.com/datapack/terratonic

  [issues]: https://github.com/RussDev7/AutoBiomeScanner/issues
  [discussions]: https://github.com/RussDev7/AutoBiomeScanner/discussions
  
<!-- Extensions -->
  [chrome_violentmonkey]: https://chrome.google.com/webstore/detail/violent-monkey/jinjaccalgkegednnccohejagnlnfdag
  [chrome_tampermonkey]: https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkealhmkfjojejmpbldmpobfkfo
  [firefox_greasemonkey]: https://addons.mozilla.org/firefox/addon/greasemonkey/
  [firefox_tampermonkey]: https://addons.mozilla.org/firefox/addon/tampermonkey/
  [firefox_violentmonkey]: https://addons.mozilla.org/firefox/addon/violentmonkey/
  [safari_tampermonkey]: https://github.com/victornpb/undiscord/issues/91#issuecomment-654514364
  [edge_tampermonkey]: https://microsoftedge.microsoft.com/addons/detail/tampermonkey/iikmkjmpaadaobahmlepeloendndfphd
  [opera_tampermonkey]: https://addons.opera.com/extensions/details/tampermonkey-beta/
  [opera_violentmonkey]: https://addons.opera.com/extensions/details/violent-monkey/

<!-- Download links -->
  [greasyfork_url]: <https://greasyfork.org/en/scripts/525551-auto-biome-scanner> "Get AutoBiomeScanner from GreasyFork"
