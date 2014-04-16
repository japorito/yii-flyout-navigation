yii-flyout-navigation
=====================

A yii widget wrapper for the jquery plugin by Justin Ross. Demo and original plugin available here: http://justinross.github.io/jquery-flyout/

Installation
=====================
Copy yii-flyout-navigation to the extensions folder of your yii application.

Usage
=====================
Call widget() with 'application.extensions.yii-flyout-navigation.FlyoutNav' as the first argument and and array of the arguments to the flyout plugin as the second argument.

The argument array must have (at a minimum) a key named 'list' whose value is an array of the html elements you want to "fly out" from the main button and a key named 'mainButton' which is the html element of the main button.
The argument array may also have arguments specifying flyout radius, degree for starting and ending the flyout, and the order to fly in and out (as well as any of the other arguments to the plugin.)

Example use:
	$this->widget('application.extensions.flyoutnav.FlyoutNav', array(
		'list'=>array(
				CHtml::link(
				CHtml::image(Yii::App()->request->baseUrl . '/images/people.svg'),
				array('index/people')
			),
			CHtml::link(
				CHtml::image(Yii::App()->request->baseUrl . '/images/map.svg'),
				array('index/people')
			),
			CHtml::link(
				CHtml::image(Yii::App()->request->baseUrl . '/images/info.svg'),
				array('index/people')
			),
			CHtml::link(
				CHtml::image(Yii::App()->request->baseUrl . '/images/calendar.svg'),
				array('index/people')
			),
		),
		'mainButton'=>CHtml::image(Yii::App()->baseUrl . '/images/touch.svg'),
		'radius'=>90,
		'totalDegrees'=>180
    );
    
    
    You will probably want to use CSS to style your widget. An example CSS file is in the examples folder. Each individual element is stored in a <li> tag. The collection of elements is stored in a <ul> tag with the id 'flyoutNav'. The main button element has the id 'mainButton'.
    
