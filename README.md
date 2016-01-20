# joomlaFields
Joomla form field to add multiple, dynamic checkboxes from database. Only for developers.

You can use this field in both site and admin component by calling:

# Admin side:
JForm::addFieldPath(JPATH_COMPONENT_ADMINISTRATOR . '/models/fields');

# Site side:
JForm::addFieldPath(JPATH_COMPONENT . '/models/fields');

and like other form field in your form xml file like this:
		<field
			name="topic_id"
			type="SQLcheckBoxes"
			label="Select an article"
			query="SELECT id, title FROM #__topics"
			key_field="id"
			value_field="title"
			required="true"
			multiple="true"
		>

