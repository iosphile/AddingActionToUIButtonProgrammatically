####AddingActionToUIButtonProgrammatically ####


import UIKit
class ViewController: UIViewController {
    
    // Declaration button
    var button: UIButton!

    override func viewDidLoad() {
        super.viewDidLoad()
        // view background color to dark gray
        self.view.backgroundColor = UIColor.darkGray
        
        // Initialization button with type system
        button = UIButton(type: UIButtonType.system)
        
        // Creating frame for button using CGRect CGFloat
        button.frame = CGRect(x: 0, y: 0, width: 150, height: 60)
        
        // Center button horizontally and vertically
        button.center.x = self.view.center.x
        button.center.y = self.view.center.y
        
        // Creating background color as yellow
        button.backgroundColor = UIColor.yellow
        
        // Creating tint color as orange
        button.tintColor = UIColor.orange
        
        // Set title for button
        button.setTitle("Button Action", for: UIControlState.normal)
        
        // Adding action to button using addTarget method
        button.addTarget(self, action: #selector(ViewController.actionButton(_:)), for: UIControlEvents.touchUpInside)
        
        // Adding button to view
        self.view.addSubview(button)
        
        
        
    }
    
    func actionButton(_ actionButton: UIButton!) {
        
        // Changing title color
        button.setTitleColor(.blue, for: UIControlState.normal)
    
    }
}
