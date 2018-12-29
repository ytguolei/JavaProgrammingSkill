# JavaProgrammingSkill

JAVA LIST去重
result = new ArrayList<Map<String, Object>>(new HashSet<Map<String, Object>>(result));

JAVA LIST查找
import org.apache.commons.beanutils.BeanPredicate;
import org.apache.commons.collections.CollectionUtils;
import org.apache.commons.collections.Predicate;
import org.apache.commons.collections.PredicateUtils;
import org.apache.commons.collections.functors.EqualPredicate;


 EqualPredicate firstNameEqlPredicate = new EqualPredicate("ganesh");
 BeanPredicate firtsNameBeanPredicate = new BeanPredicate("firstName", firstNameEqlPredicate);
 EqualPredicate lastNameEqlPredicate2 = new EqualPredicate("gowtham");
 BeanPredicate lastNameBeanPredicate2 = new BeanPredicate("lastName", lastNameEqlPredicate2);
 Predicate[] allPredicateArray = {firtsNameBeanPredicate, lastNameBeanPredicate2};
 Predicate allPredicate = PredicateUtils.allPredicate(allPredicateArray);
 Collection<Person> filteredCollection = CollectionUtils.select(personList, allPredicate);
