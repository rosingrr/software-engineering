package com.example.sympmeds;

import android.os.Bundle;
import android.app.Activity;
import android.content.Intent;
import android.view.Menu;
import android.view.View;
import android.widget.ArrayAdapter;
import android.widget.Spinner;

public class DrugList extends Activity {
	public final static String DRUG_INFO = "com.example.sympmeds.INFO";

	@Override
	protected void onCreate(Bundle savedInstanceState) {
		super.onCreate(savedInstanceState);
		setContentView(R.layout.activity_drug_list);
		
        Spinner spinner = (Spinner) findViewById(R.id.spinner2);
        ArrayAdapter<CharSequence> adapter = ArrayAdapter.createFromResource(
        		this, R.array.drug_list, android.R.layout.simple_spinner_item);
        adapter.setDropDownViewResource(android.R.layout.simple_spinner_dropdown_item);
        spinner.setAdapter(adapter);
	}

	@Override
	public boolean onCreateOptionsMenu(Menu menu) {
		// Inflate the menu; this adds items to the action bar if it is present.
		getMenuInflater().inflate(R.menu.drug_list, menu);
		return true;
	}
	
    /** Called when the user clicks the Get Info button */
    public void getInfo (View view) {
    	// Do something in response to button}
		Intent intent = new Intent(this, DrugInfo.class);
		Spinner spinner = (Spinner) findViewById(R.id.spinner2);
		String text = spinner.getSelectedItem().toString();
		try {
			intent.putExtra(DRUG_INFO, text);
		} catch (Exception e) {
		     // This will catch any exception, because they are all descended from Exception
		}
		startActivity(intent);
    }

}
