<?php
/**
 * @project mod_randomize
 * @author Nicholas K. Dionysopoulos http://www.dionysopoulos.me
 * @license GNU General Public License, version 3 of the license or - at your option - any later version
 * @copyright Copyright (c)2010 Nicholas K. Dionysopoulos. All rights reserved.
 *
 * A module to display a single randomly choosed module out of an entire Joomla! module position
 */

$position = $params->get('position','left');
$style = $params->get('style','random');
if(empty($position)) return;
if(empty($style)) $style="random";

$modules = JModuleHelper::getModules($position);
$attribs = array('style'=>$style);

if(empty($modules)) return '';

$numModules = count($modules);
$index = rand(0, $numModules-1);
$module = $modules[$index];
echo $module->content;
//echo JModuleHelper::renderModule( $module, $attribs );