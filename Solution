
import java.util.List;


public class Solution {
    int index = 0;

    public NestedInteger deserialize(String s) {
        if (s.charAt(index) == '[') {
            index++;
            NestedInteger ni = new NestedInteger();
            while (s.charAt(index) != ']') {
                ni.add(deserialize(s));
                if (s.charAt(index) == ',') {
                    index++;
                }
            }
            index++;
            return ni;
        } else {
            boolean negative = false;
            if (s.charAt(index) == '-') {
                negative = true;
                index++;
            }
            int num = 0
            if (negative) {
                num = (-1)*Integer.parseInt(s.split("-")[1]);
            }else {
                num = Integer.parseInt(s)
            }
            return new NestedInteger(num);
        }
}
