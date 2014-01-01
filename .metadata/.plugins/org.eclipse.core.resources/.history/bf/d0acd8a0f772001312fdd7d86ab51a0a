package br.com.androidzin.android_examples;

import java.util.ArrayList;
import java.util.List;

import android.os.Bundle;
import android.text.InputFilter;
import android.text.Spanned;
import android.widget.EditText;
import android.widget.SpinnerAdapter;

import com.actionbarsherlock.app.ActionBar;
import com.actionbarsherlock.app.ActionBar.OnNavigationListener;
import com.actionbarsherlock.app.SherlockActivity;
import com.actionbarsherlock.view.Menu;

public class SpinnerIconActivity extends SherlockActivity implements OnNavigationListener{

	private SpinnerAdapter mSpinnerAdapter;
	@Override
	protected void onCreate(Bundle savedInstanceState) {
		super.onCreate(savedInstanceState);
		setContentView(R.layout.activity_spinner_icon);
		
		ActionBar actionBar = getSupportActionBar();
		actionBar.setNavigationMode(ActionBar.NAVIGATION_MODE_LIST);
		
		
		List<SpinnerRow> options = new ArrayList<SpinnerRow>();
		options.add(new SpinnerRow("Droid 1", R.drawable.android01));
		options.add(new SpinnerRow("Droid 2", R.drawable.android02));
		options.add(new SpinnerRow("Droid 3", R.drawable.android03));
		mSpinnerAdapter  = new MySpinnerAdapter(getApplicationContext(),
				R.layout.spinner_row, R.id.text, options);
		
		actionBar.setListNavigationCallbacks(mSpinnerAdapter, this);
		
		EditText t = (EditText) findViewById(R.id.teste);
		InputFilter filter = new InputFilter() { 
			
			@Override
			public CharSequence filter(CharSequence source, int start, int end,
					Spanned dest, int dstart, int dend) {
				for (int i = start; i < end; i++) { 
					if (!Character.isLetter(source.charAt(i))) { 
						return ""; 
					} 
				} 
				return null;
			} 
		}; 
		t.setFilters(new InputFilter[]{filter});

	 
	}

	@Override
	public boolean onCreateOptionsMenu(Menu menu) {
		getSupportMenuInflater().inflate(R.menu.main, menu);
		return super.onCreateOptionsMenu(menu);
	}

	@Override
	public boolean onNavigationItemSelected(int itemPosition, long itemId) {
		return false;
	}

}
