# AT Lab

## Alert Dialog
AlertDialog.Builder ab = new AlertDialog.Builder(MainActivity2.this);

ab.setTitle("Darshaan");
ab.setMessage("do you really want to do this?");

ab.setPositiveButton("Yes", new DialogInterface.OnClickListener() {
@Override
public void onClick(DialogInterface dialog, int which) {
Toast.makeText(MainActivity2.this, "Thanks!", Toast.LENGTH_SHORT).show();
}
});

ab.setNegativeButton("no", null);
<b>ab.show();</b>
});

## Button
Button button = findViewById(R.id.button);
button.setOnClickListener((v)->{
});


## Toast
Toast.makeText(MainActivity.this, "You clicked a button", Toast.LENGTH_SHORT).show();

## Intent
Intent intent = new Intent(MainActivity.this, MainActivity2.class);

intent.putExtra("name", "Sathwik");
intent.putExtra("age", 21);

startActivity(intent);

// In the other activity

String name = getIntent().getStringExtra("name");

## spin

String[] colorss={"Select", "Blue", "Black"};
spin=findViewById(R.id.spinner);
ArrayAdapter<String> adapter=new ArrayAdapter<>(this, android.R.layout.simple_spinner_dropdown_item, colorss);
spin.setAdapter(adapter);

spin.setOnItemSelectedListener(new AdapterView.OnItemSelectedListener() {
    @Override
    public void onItemSelected(AdapterView<?> parent, View view, int position, long id) {
        String selected=colorss[position];
        if(selected=="Blue"){
            mainlayout.setBackgroundColor(Color.BLUE);
        }
        else if(selected=="Black"){
            mainlayout.setBackgroundColor(Color.BLACK);
        }
        else{
            mainlayout.setBackgroundColor(Color.WHITE);
        }
        res.setLength(0);
        res.append("Selected Color: ").append(selected);
        textt.setText(res);

}
@Override
public void onNothingSelected(AdapterView<?> parent) {
    mainlayout.setBackgroundColor(Color.WHITE);
}
});

## list (colorss array and adapter used from "spin")

listi= findViewById(R.id.listt);
        listi.setAdapter(adapter);
listi.setOnItemClickListener(new AdapterView.OnItemClickListener() {
    @Override
    public void onItemClick(AdapterView<?> parent, View view, int position, long id) {
        String si=colorss[position];
        Toast.makeText(MainActivity.this, "Selected: "+ si, Toast.LENGTH_SHORT).show();
    }
});

