// calculater kod dökümü .



package calculate;

import java.awt.EventQueue;

import javax.swing.JFrame;
import javax.swing.JPanel;
import javax.swing.border.EmptyBorder;
import javax.xml.validation.TypeInfoProvider;
import javax.swing.JTextField;
import java.awt.Font;
import javax.swing.SwingConstants;
import java.awt.GridLayout;

import javax.swing.InputMap;
import javax.swing.JButton;
import java.awt.event.ActionListener;
import java.nio.channels.IllegalBlockingModeException;
import java.security.PublicKey;
import java.awt.event.ActionEvent;
import java.awt.Color;
import javax.swing.JLabel;

public class guitest extends JFrame {

	private static final long serialVersionUID = 1L;
	private JPanel contentPane;
	private JTextField input;
	private double number,result;
 	private  int operation  ;
	/**
	 * Launch the application.
	 */
	public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					guitest frame = new guitest();
					frame.setVisible(true);
				} catch (Exception e) {
					e.printStackTrace();
				}
			}
		});
	}
    public void addInput(String str) {
		input.setText(input.getText()+str);	
	
		
		
	}
	// hesaplama işlemini yapan fonksiyon .

 
	public void calculater() {
		switch (operation) {
		case 1: {
			result=number+Double.parseDouble(input.getText());
			input.setText(Double.toString(result));
			;
               break;
		}
		case 2: {
			result=number-Double.parseDouble(input.getText());
					input.setText(Double.toString(result));
			break;
					
		}case 3: {
			result=number*Double.parseDouble(input.getText());
					input.setText(Double.toString(result));
			break;
		}case 4: {
			result=number/Double.parseDouble(input.getText());
					input.setText(Double.toString(result));
			break;
		}
		
		
		}
		
		
	}
	
	
	
	// frame oluşturma 
	 
	public guitest() {
		setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		setBounds(100, 100, 400, 542);
		contentPane = new JPanel();
		contentPane.setBorder(new EmptyBorder(5, 5, 5, 5));

		setContentPane(contentPane);
		contentPane.setLayout(null);
		
		JPanel panel_2 = new JPanel();
		panel_2.setBounds(158, 14, 1, 1);
		contentPane.add(panel_2);
		panel_2.setLayout(null);
		
		JPanel panel = new JPanel();
		panel.setBounds(179, 14, 1, 1);
		contentPane.add(panel);
		panel.setLayout(null);
		
		JPanel screen = new JPanel();
		screen.setBounds(10, 14, 366, 56);
		contentPane.add(screen);
		screen.setLayout(null);
		
		input = new JTextField();
		input.setBounds(0, 19, 366, 37);
		input.setEditable(false);
		input.setHorizontalAlignment(SwingConstants.RIGHT);
		input.setFont(new Font("Bodoni MT Black", Font.BOLD, 26));
		screen.add(input);
		input.setColumns(10);
		
		JLabel lblNewLabel = new JLabel("New label");
		lblNewLabel.setBounds(321, 10, -42, -1);
		screen.add(lblNewLabel);
		
		JLabel lbl = new JLabel("");
		lbl.setHorizontalAlignment(SwingConstants.RIGHT);
		lbl.setFont(new Font("Tahoma", Font.BOLD, 15));
		lbl.setBounds(0, 0, 356, 22);
		screen.add(lbl);
		
		JPanel panel_1 = new JPanel();
		panel_1.setBounds(10, 90, 366, 415);
		contentPane.add(panel_1);
		panel_1.setLayout(new GridLayout(4, 4, 20, 20));

  	 //  hesap makinesinin sayılar ve işlemler kısmının gösterilmesi . 

  
		JButton btnNewButton_1 = new JButton("7");
		btnNewButton_1.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				   addInput(e.getActionCommand()); 
			}
		});
		btnNewButton_1.setFont(new Font("Tahoma", Font.BOLD, 23));
		panel_1.add(btnNewButton_1);
		
		JButton btnNewButton_2 = new JButton("8");
		btnNewButton_2.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				   addInput(e.getActionCommand()); 
			}
		});
		btnNewButton_2.setFont(new Font("Tahoma", Font.BOLD, 23));
		panel_1.add(btnNewButton_2);
		
		JButton btnNewButton_3 = new JButton("9");
		btnNewButton_3.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				   addInput(e.getActionCommand()); 
			}
		});
		btnNewButton_3.setFont(new Font("Tahoma", Font.BOLD, 23));
		panel_1.add(btnNewButton_3);
		
		JButton btnNewButton_6 = new JButton("+");
		btnNewButton_6.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
					number= Double.parseDouble(input.getText());
					operation=1 ;		
			         input.setText(" ");
			lbl.setText(number+ e.getActionCommand());
			}        
		});
		btnNewButton_6.setFont(new Font("Tahoma", Font.BOLD, 23));
		panel_1.add(btnNewButton_6);
		
		JButton btnNewButton_7 = new JButton("4");
		btnNewButton_7.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				   
				addInput(e.getActionCommand()); 	}
		});
		btnNewButton_7.setFont(new Font("Tahoma", Font.BOLD, 23));
		panel_1.add(btnNewButton_7);
		
		JButton btnNewButton_9 = new JButton("5");
		btnNewButton_9.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				   addInput(e.getActionCommand()); 
			}
		});
		btnNewButton_9.setFont(new Font("Tahoma", Font.BOLD, 23));
		panel_1.add(btnNewButton_9);
		
		JButton btnNewButton_8 = new JButton("6");
		btnNewButton_8.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				   addInput(e.getActionCommand()); 
			}
		});
		btnNewButton_8.setFont(new Font("Tahoma", Font.BOLD, 23));
		panel_1.add(btnNewButton_8);
		
		JButton btnX = new JButton("X");
		btnX.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
			
				number= Double.parseDouble(input.getText());
				operation=3;		
		         input.setText(" ");
		lbl.setText(number+ e.getActionCommand());
			}
		});
		btnX.setFont(new Font("Tahoma", Font.BOLD, 23));
		panel_1.add(btnX);
		
		JButton btnNewButton_11 = new JButton("1");
		btnNewButton_11.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				   addInput(e.getActionCommand()); 
			}
		});
		btnNewButton_11.setFont(new Font("Tahoma", Font.BOLD, 23));
		panel_1.add(btnNewButton_11);
		
		JButton btnNewButton_13 = new JButton("2");
		btnNewButton_13.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
			
				   addInput(e.getActionCommand()); }
		});
		btnNewButton_13.setFont(new Font("Tahoma", Font.BOLD, 23));
		panel_1.add(btnNewButton_13);
		
		JButton btnNewButton_14 = new JButton("3");
		btnNewButton_14.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {  
				addInput(e.getActionCommand()); 
			}
		});
		btnNewButton_14.setFont(new Font("Tahoma", Font.BOLD, 23));
		panel_1.add(btnNewButton_14);
		
		JButton btnNewButton_17 = new JButton("-");
		btnNewButton_17.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				   
				number= Double.parseDouble(input.getText());
				operation=2 ;		
		         input.setText(" ");
		lbl.setText(number+ e.getActionCommand());
			}
		});
		btnNewButton_17.setFont(new Font("Tahoma", Font.BOLD, 23));
		panel_1.add(btnNewButton_17);
		
		JButton btnNewButton_16 = new JButton("=");
		btnNewButton_16.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) { 
				
			calculater();
			lbl.setText(" ");
			}
		});
		btnNewButton_16.setFont(new Font("Tahoma", Font.BOLD, 23));
		panel_1.add(btnNewButton_16);
		
		JButton btnNewButton_15 = new JButton("0");
		btnNewButton_15.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
			   addInput(e.getActionCommand()); 
			
			
			}
		});
		btnNewButton_15.setBackground(new Color(240, 240, 240));
		btnNewButton_15.setFont(new Font("Tahoma", Font.BOLD, 23));
		panel_1.add(btnNewButton_15);
		
		JButton btnC = new JButton("C");
		btnC.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				  input.setText("");
			}
		});
		btnC.setFont(new Font("Tahoma", Font.BOLD, 23));
		panel_1.add(btnC);
		
		JButton btnNewButton_19 = new JButton("/");
		btnNewButton_19.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				 
				number= Double.parseDouble(input.getText());
				operation=4 ;		
		         input.setText(" ");
		lbl.setText(number+ e.getActionCommand());
			}
		});
		btnNewButton_19.setFont(new Font("Tahoma", Font.BOLD, 23));
		panel_1.add(btnNewButton_19);
	}
}
